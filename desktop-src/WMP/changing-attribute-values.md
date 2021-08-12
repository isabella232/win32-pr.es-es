---
title: Cambiar valores de atributo
description: Cambiar valores de atributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Reproductor de Windows Media,attributes para elementos multimedia
- Reproductor de Windows Media modelo de objetos, atributos para elementos multimedia
- object model,attributes for media items
- Reproductor de Windows Media Móvil, atributos para elementos multimedia
- Reproductor de Windows Media ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media Control de ActiveX móviles,atributos para elementos multimedia
- ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media biblioteca,atributos para elementos multimedia
- library,attributes para elementos multimedia
- attributes,changing values
- cambiar valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870d8bfa13012bd79fdd672f1543db4a484ca5d9674ef1a9e48e832119ea1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581121"
---
# <a name="changing-attribute-values"></a>Cambiar valores de atributo

Puede cambiar el valor de un atributo si la página web o aplicación tiene acceso de lectura y escritura a la biblioteca y el atributo puede ser de lectura y escritura.

Puede cambiar un atributo del elemento multimedia actual. Para cambiar los atributos de varios elementos multimedia, puede asignar cada uno a su vez al *reproductor*. **propiedad currentMedia.**

A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Para cambiar un atributo, llame al *reproductor*. *currentMedia*. **Método setItemInfo** como se muestra en el siguiente ejemplo de C#.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Se recomienda llamar a *Media*. **Método isReadOnlyItem** para determinar si se puede cambiar un atributo determinado.

> [!Note]  
> Si inserta el control en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Reproductor de Windows Media. Si usa el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios. En cualquier caso, los cambios están disponibles inmediatamente a través de la biblioteca.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elementos multimedia**](media-item-attributes.md)
</dt> <dt>

[**Acceso a la biblioteca**](library-access.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Lectura de valores de atributo**](reading-attribute-values.md)
</dt> </dl>

 

 




