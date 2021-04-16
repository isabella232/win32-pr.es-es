---
title: Atributo DLNAServerUDN
description: El atributo DLNAServerUDN es el nombre de dispositivo único del servidor que hospeda el elemento multimedia.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- DLNAServerUDN Media Player de Windows
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699887"
---
# <a name="dlnaserverudn-attribute"></a>Atributo DLNAServerUDN

El atributo **DLNAServerUDN** es el nombre de dispositivo único del servidor que hospeda el elemento multimedia.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotografía**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual. Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica. Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





