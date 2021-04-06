---
title: Cambiar valores de atributo
description: Cambiar valores de atributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, cambiar valores
- cambiar valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075873"
---
# <a name="changing-attribute-values"></a>Cambiar valores de atributo

Puede cambiar el valor de un atributo si su página web o aplicación tiene acceso de lectura y escritura a la biblioteca y el atributo se puede leer y escribir.

Puede cambiar un atributo del elemento multimedia actual. Para cambiar los atributos de varios elementos multimedia, puede asignar cada uno de ellos a su vez al *reproductor*. propiedad **currentMedia** .

A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Para cambiar un atributo, llame al *reproductor*. *currentMedia*. método **setItemInfo** tal como se muestra en el siguiente ejemplo de C#.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Se recomienda llamar a los *medios*. método **isReadOnlyItem** para determinar si se puede cambiar un atributo determinado.

> [!Note]  
> Si incrusta el control en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Windows Media Player. Si utiliza el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios. En cualquier caso, los cambios están disponibles inmediatamente a través de la biblioteca.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elemento multimedia**](media-item-attributes.md)
</dt> <dt>

[**Acceso a bibliotecas**](library-access.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> </dl>

 

 




