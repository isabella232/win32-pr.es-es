---
title: Atributo DLNASourceURI
description: El atributo DLNASourceURI es el identificador de recursos universal (URI) del elemento.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- DLNASourceURI Media Player de Windows
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699580"
---
# <a name="dlnasourceuri-attribute"></a>Atributo DLNASourceURI

El atributo **DLNASourceURI** es el identificador de recursos universal (URI) del elemento.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Otros elementos**](other-item-attributes.md)
-   [**Elementos de fotografía**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Si el elemento se encuentra en la biblioteca local del usuario actual, este atributo, el atributo [**SourceURL**](sourceurl-attribute.md) y el valor devuelto por [**IWMPMedia:: get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) son los mismos.

Si el elemento no está en la biblioteca local del usuario actual, pero pertenece a una biblioteca remota, este atributo es un identificador con el formato DLNA-playsingle://*XXX*.

Puede pasar un URI DLNA-playsingle al método [**IWMPCore3:: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) para obtener una interfaz [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) que le permita ver los metadatos del elemento multimedia y modificar potencialmente la clasificación de estrellas del elemento multimedia. Sin embargo, tenga en cuenta que el URI DLNA-playsingle debe ser para un servicio de directorio de contenido (CDS) que Windows Media Player ya haya detectado. El método **newMedia** no iniciará la detección de UPnP y buscará los CD.

Solo puede editar la clasificación por estrellas de un elemento multimedia en una biblioteca remota si la biblioteca remota admite la operación de edición. Las bibliotecas remotas hospedadas en un equipo que ejecuta Windows 7 admiten la operación de edición. Las bibliotecas remotas hospedadas en un equipo que ejecuta un sistema operativo Windows anterior a Windows 7 no admiten la operación de edición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





