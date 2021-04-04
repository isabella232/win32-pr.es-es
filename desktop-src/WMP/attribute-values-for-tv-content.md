---
title: Valores de atributo para el contenido de TV
description: Valores de atributo para el contenido de TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
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
- atributos, contenido de TV
- Valores de atributo de contenido de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076359"
---
# <a name="attribute-values-for-tv-content"></a>Valores de atributo para el contenido de TV

A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 o posterior pueden organizar el contenido de la televisión en la biblioteca. Windows Media Player trata el contenido de TV como subcategoría del contenido de vídeo. Para que el contenido de vídeo aparezca en los nodos de TV de la biblioteca, establezca los atributos **WM/MediaClassPrimaryID** y **WM/MediaClassSecondaryID** en los valores de la tabla siguiente mediante el uso de los *medios*. método **setItemInfo** :



| Atributo                    | Value                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

También puede usar estos valores para determinar si un determinado elemento multimedia digital contiene contenido de TV mediante el uso de los *medios*. **getItemInfo** o *multimedia*. métodos de **getItemInfoByType** .

Recuerde usar los valores de **GUID** como valores de **cadena** al especificar o recuperar estos valores.

El siguiente código de ejemplo de C# establece los atributos de la clase multimedia para que un elemento multimedia se identifique como contenido de TV.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Para obtener más información sobre los posibles valores de los atributos de la clase multimedia, vea las directrices de uso de los [metadatos de Windows Media](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elemento multimedia**](media-item-attributes.md)
</dt> <dt>

[**Acceso a bibliotecas**](library-access.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 




