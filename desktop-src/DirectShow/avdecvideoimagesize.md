---
description: Obtiene el tamaño de la imagen descodificada, en píxeles.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Propiedad AVDecVideoImageSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4c059dfb1b2aebad4da10e54a3ecc1224a00d9cffcdb13dc7c87f4e29d4e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000195"
---
# <a name="avdecvideoimagesize-property"></a>Propiedad AVDecVideoImageSize

Obtiene el tamaño de la imagen descodificada, en píxeles.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoImageSize**

## <a name="property-value"></a>Valor de propiedad

Los 16 bits altos contienen el ancho y los 16 bits inferiores contienen el alto.

## <a name="remarks"></a>Comentarios

El número de canales incluye el canal de efecto de baja frecuencia (LFE), si está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




