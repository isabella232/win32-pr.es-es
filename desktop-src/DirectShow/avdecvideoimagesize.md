---
description: Obtiene el tamaño de la imagen descodificada, en píxeles.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Propiedad AVDecVideoImageSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162101"
---
# <a name="avdecvideoimagesize-property"></a>Propiedad AVDecVideoImageSize

Obtiene el tamaño de la imagen descodificada, en píxeles.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoImageSize**

## <a name="property-value"></a>Valor de propiedad

Los 16 bits altos contienen el ancho y los 16 bits bajos contienen el alto.

## <a name="remarks"></a>Observaciones

El número de canales incluye el canal de efecto de baja frecuencia (LFE), si está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




