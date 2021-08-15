---
description: Especifica si el codificador principal usa el &\# 0034; Además&\# característica 0034;.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab3fdcd3087773ea760615224b148bd497c1f89114c0f761a7d2f90fb0b5a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738022"
---
# <a name="mfpkey_enhanced_wma-property"></a>Propiedad \_ WMA MEJORADA de MFPKEY \_

Especifica si el codificador principal usa la característica "Más".

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad solo está disponible para Windows audio multimedia sin pérdida.

Si deja esta propiedad en su valor predeterminado de 0 o si la establece en 1, el codificador principal decide si se debe usar la parte "Más". Si establece esta propiedad en 2, el codificador principal no usa la característica "Más".

Esta propiedad modifica los tipos de medios enumerados, por lo que si lo establece, debe hacerlo antes de establecer el tipo de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
