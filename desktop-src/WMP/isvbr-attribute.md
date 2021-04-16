---
title: Atributo IsVBR
description: El atributo IsVBR indica si el contenido se ha codificado mediante la codificación de velocidad de bits variable (VBR).
ms.assetid: faec0940-ef53-40a1-be54-a990884e907d
keywords:
- IsVBR Media Player de Windows
topic_type:
- apiref
api_name:
- IsVBR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaec9f740e7b251c73ed12f5897ff9d95b023886
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690488"
---
# <a name="isvbr-attribute"></a>Atributo IsVBR

El atributo **IsVBR** indica si el contenido se ha codificado mediante la codificación de velocidad de bits variable (VBR).

## <a name="applies-to"></a>Se aplica a

-   [Archivos de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en el archivo multimedia digital.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMIsVBR.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





