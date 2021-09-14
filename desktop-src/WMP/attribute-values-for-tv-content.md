---
title: Valores de atributo para contenido de TV
description: Valores de atributo para contenido de TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Reproductor de Windows Media,atributos para elementos multimedia
- Reproductor de Windows Media modelo de objetos, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Reproductor de Windows Media Móvil, atributos para elementos multimedia
- Reproductor de Windows Media ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media Control de ActiveX móviles, atributos para elementos multimedia
- ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media biblioteca, atributos para elementos multimedia
- library,attributes para elementos multimedia
- attributes,TV content
- Valores de atributo de contenido de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241077"
---
# <a name="attribute-values-for-tv-content"></a>Valores de atributo para contenido de TV

A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Reproductor de Windows Media 10 o posterior puede organizar el contenido de la televisión en la biblioteca. Reproductor de Windows Media el contenido de televisión como una subcategoría de contenido de vídeo. Para que el contenido del vídeo aparezca en los nodos de TV de la biblioteca, establezca los atributos **WM/MediaClassPrimaryID** y **WM/MediaClassSecondaryID** en los valores de la tabla siguiente mediante el uso del medio *.* **Método setItemInfo:**



| Atributo                    | Value                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

También puede usar estos valores para determinar si un elemento multimedia digital determinado contiene contenido de televisión mediante el *medio*. **getItemInfo o** *multimedia*. **Métodos getItemInfoByType.**

Recuerde usar los valores **GUID** como valores **de cadena** al especificar o recuperar estos valores.

El siguiente código de ejemplo de C# establece los atributos de clase multimedia para que un elemento multimedia se identifique como contenido de televisión.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Para obtener más información sobre los valores posibles para los atributos de clase multimedia, vea el Windows instrucciones de uso de [metadatos multimedia](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elementos multimedia**](media-item-attributes.md)
</dt> <dt>

[**Acceso a la biblioteca**](library-access.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 




