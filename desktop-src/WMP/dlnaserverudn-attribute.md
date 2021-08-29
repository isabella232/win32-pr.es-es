---
title: Atributo DLNAServerUDN
description: El atributo DLNAServerUDN es el nombre de dispositivo único del servidor que hospeda el elemento multimedia.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Atributo DLNAServerUDN Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7e88b29f53acf06553b5ff1126d438f67d775f3f7a5341a00b9c19f0199b6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997225"
---
# <a name="dlnaserverudn-attribute"></a>Atributo DLNAServerUDN

El **atributo DLNAServerUDN** es el nombre de dispositivo único del servidor que hospeda el elemento multimedia.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para elementos multimedia que pertenecen a una biblioteca remota; es decir, una biblioteca que otro usuario ha puesto a disposición de los usuarios en la red doméstica. Para determinar si una biblioteca multimedia es remota, llame al [**tipo IWMPLibrary::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





