---
title: Atributo DLNASourceURI
description: El atributo DLNASourceURI es el identificador de recursos universal (URI) del elemento.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Atributo DLNASourceURI Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e5383de75fef1a0e1957f270a8a5238951bce4ede1418dbf79ba2038777372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997175"
---
# <a name="dlnasourceuri-attribute"></a>Atributo DLNASourceURI

El **atributo DLNASourceURI** es el identificador de recursos universal (URI) del elemento.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Otros elementos**](other-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Si el elemento está en la biblioteca local del usuario actual, este atributo, el atributo [**SourceURL**](sourceurl-attribute.md) y el valor devuelto por [**IWMPMedia::get \_ sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) son todos iguales.

Si el elemento no está en la biblioteca local del usuario actual, pero pertenece a una biblioteca remota, este atributo es un identificador con el formato dlna-playsingle://*xxx*.

Puede pasar un URI dlna-playsingle al método [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) para obtener una interfaz [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) que le permita ver los metadatos del elemento multimedia y posiblemente editar la clasificación de estrellas del elemento multimedia. Sin embargo, tenga en cuenta que el URI dlna-playsingle debe ser para un servicio de directorio de contenido (CDS) que Reproductor de Windows Media haya detectado. El **método newMedia** no iniciará la detección de UPnP y buscará el CDS.

Puede editar la clasificación de estrella de un elemento multimedia en una biblioteca remota solo si la biblioteca remota admite la operación de edición. Las bibliotecas remotas hospedadas en un equipo Windows 7 admiten la operación de edición. Las bibliotecas remotas hospedadas en un equipo que ejecuta Windows sistema operativo anterior a Windows 7 no admiten la operación de edición.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





