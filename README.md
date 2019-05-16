# Shape.lua
A lua class I often use when making games

Example of it being used with the [LOVE framework](https://www.love2d.org)
```lua
Player = class(
    Shape,
    function(self)
        self.image = love.graphics.newImage("player.png")
        Shape.init(self, 100, 100, self.image:getWidth(), self.image:getHeight())
        -- also possible to do Shape.init(self, 100, 100, self.image:getDimensions)
    end
)

function Player:draw()
    -- as you can see, there was no need to define the self.x in the player constructor, 
    -- as it was already initialised in Shape
    love.graphics.draw(self.image, self.x, self.y)
end
```
