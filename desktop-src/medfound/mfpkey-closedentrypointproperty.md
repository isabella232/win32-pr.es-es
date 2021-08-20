---
description: Especifica el patrón de codificación que el codificador usará al principio de un grupo de imágenes.
ms.assetid: 0744fdd5-8bff-47a9-ae97-90637d91ff37
title: MFPKEY_CLOSEDENTRYPOINT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da5d351d0189cb0637e15a89c5108e42ccf5629863a298a624baa13ed581c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873596"
---
# <a name="mfpkey_closedentrypoint-property"></a>Propiedad MFPKEY \_ CLOSEDENTRYPOINT

Especifica el patrón de codificación que el codificador usará al principio de un grupo de imágenes.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCClosedEntryPoint**

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Si establece esta propiedad en **VARIANT \_ TRUE,** el patrón de codificación es BBIBBP. Si establece esta propiedad en **VARIANT \_ FALSE,** el patrón de codificación es IBBPBBP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




