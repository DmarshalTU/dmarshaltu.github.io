![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*FpWQ8XB29XIplUJNMkAm0Q.png)


[Simon Marache](https://github.com/Blizarre) [MicroDalle](https://github.com/Blizarre/microdalle.git) project suited me very well because of his use of the openai library in Python and flask, at first glance the project seemed lost because I could not find any library that allowed me to work with the chatgpt api, on the other hand I did not know in crystal any framework for building servers and worst of all I haven't written anything for more than 3 months because of reserve service and I really had no desire to go back to sitting in front of the computer and especially not writing code.
But this project gave me back my desire to explore and opened up a new horizon, to take a rich, easy-to-learn language and write the libraries and the project myself without just importing existing things, on one screen the library with the debugger and on the other side the server that is based on the same library, because I immersed myself in the crystal syntax and in the book The only one I found was "Crystal Programming" by George Dietrich and both projects were written as one.
Another good thing in my experience along the way is learning to work with [Kemal](https://kemalcr.com/), Lightning Fast, Super Simple web framework.

GitHub [MicroDalle_cr](https://github.com/DmarshalTU/microdallecr.git)

As I wrote in the previous article about [OpenAI Crystal Library: Bridging Machine Learning and the Crystal Language](https://medium.com/@denismarshalltumakov/openai-crystal-library-bridging-machine-learning-and-the-crystal-language-f88a9536ba0b), the OpenAI Crystal Library is focused on providing a straightforward and efficient interface for integrating OpenAI's machine learning capabilities with Crystal-based applications. It's not about reinventing the wheel; it's about building solid connections between existing technologies and learn new things.

The project made me promote the library and also add the possibility of working with photos and not just as a chat, this is what came out.

GitHub [OpenAI_CR](https://github.com/DmarshalTU/openai.git)

```crystal
require "openai"

Log.setup_from_env

OPENAI_KEY = "xxxxxxxxxx"
client = OpenAI::Client.new(OPENAI_KEY)

response = client.create_image_completion("dall-e-3", "image description", size, hd, 1)
```

in the future if this library will get to [ShardBox](https://shardbox.org/), it can be imported via dependencies:
```yaml
dependencies:
  openai:
    github: dmarshaltu/openai
```

The journey has just begun and there is still a long way to go.