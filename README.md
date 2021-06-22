input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        # # . . .
        # # # . .
        # # # # .
        # # # . .
        # # . . .
        `)
    SGBotic.playTrack(
    1,
    1
    )
})
input.onButtonPressed(Button.AB, function () {
    basic.showLeds(`
        . . . . .
        . # # # .
        . # # # .
        . # # # .
        . . . . .
        `)
    SGBotic.stop(
    )
})
input.onButtonPressed(Button.B, function () {
    basic.showLeds(`
        . # . # .
        . # . # .
        . # . # .
        . # . # .
        . # . # .
        `)
    SGBotic.pause(
    )
})
serial.onDataReceived(serial.delimiters(Delimiters.NewLine), function () {
	
})
SGBotic.MP3_init(
SerialPin.P12,
SerialPin.P13
)
SGBotic.setVolume(
16
)
basic.forever(function () {
    if (input.isGesture(Gesture.Shake)) {
        basic.showLeds(`
            # # . . .
            # # # . .
            # # # # .
            # # # . .
            # # . . .
            `)
        SGBotic.playTrack(
        1,
        1
        )
    }
})
