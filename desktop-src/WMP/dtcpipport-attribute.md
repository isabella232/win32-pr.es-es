---
title: Atributo DTCPIPPort
description: El atributo DTCPIPPort es el número de puerto del Protocolo de control de transmisión (TCP) del equipo o dispositivo en el que se debe establecer contacto para la transmisión digital Content Protection a través del Protocolo de Internet (DTCP-IP) intercambio de claves autenticado (Rear) para el elemento multimedia.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- DTCPIPPort Media Player de Windows
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700428"
---
# <a name="dtcpipport-attribute"></a>Atributo DTCPIPPort

El atributo **DTCPIPPort** es el número de puerto del Protocolo de control de transmisión (TCP) del equipo o dispositivo en el que se debe establecer contacto para la transmisión digital Content Protection a través del Protocolo de Internet (DTCP-IP) intercambio de claves autenticado (Rear) para el elemento multimedia.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotografía**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Si este atributo está disponible, el elemento multimedia se protege mediante DTCP-IP.

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica. Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





