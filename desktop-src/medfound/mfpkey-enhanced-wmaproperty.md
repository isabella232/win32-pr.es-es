---
description: Especifica si el codificador básico utiliza el &\# 0034; Más&\# 0034; característica.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Propiedad MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650192"
---
# <a name="mfpkey_enhanced_wma-property"></a>MFPKEY \_ \_ propiedad WMA mejorada

Especifica si el codificador básico usa la característica "Plus".

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad solo está disponible para Windows Media Audio sin pérdida.

Si deja esta propiedad en su valor predeterminado de 0, o si se establece en 1, el codificador principal decide si se debe usar la parte "más". Si establece esta propiedad en 2, el codificador básico no utiliza la característica "Plus".

Esta propiedad modifica los tipos de medios enumerados, por lo que si se establece, debe hacerlo antes de establecer el tipo de salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
