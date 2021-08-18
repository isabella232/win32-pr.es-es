---
title: Atributo DTCPIPHost
description: El atributo DTCPIPHost es el nombre o la dirección IP del equipo o dispositivo al que se debe ponerse en contacto para el Content Protection de transmisión digital a través del protocolo de Internet (DTCP-IP) authenticated Key Exchange (AKE) para el elemento multimedia.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Atributo DTCPIPHost Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88eaa85b756a46b1333db2e5eabda9cbaf86a702f5ae9c8225d6f6d8928e2d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996955"
---
# <a name="dtcpiphost-attribute"></a>Atributo DTCPIPHost

El atributo **DTCPIPHost** es el nombre o la dirección IP del equipo o dispositivo al que se debe ponerse en contacto para el Content Protection de transmisión digital a través del protocolo de Internet (DTCP-IP) authenticated Key Exchange (AKE) para el elemento multimedia.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Si este atributo está disponible, el elemento multimedia se protege mediante DTCP-IP.

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para elementos multimedia que pertenecen a una biblioteca remota; es decir, una biblioteca que otro usuario ha puesto a disposición de los usuarios en la red doméstica. Para determinar si una biblioteca multimedia es remota, llame al [**tipo IWMPLibrary::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





