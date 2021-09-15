---
description: Especifica si el descodificador debe realizar Lt-Rt abajo.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474081"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>Propiedad MFPKEY \_ WMADEC \_ LTRTOUTPUT

Especifica si el descodificador debe realizar Lt-Rt abajo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Observaciones

Si esta propiedad tiene un valor de VARIANT FALSE y la salida es estéreo, el descodificador de audio usa un \_ simple plegado de canales. Si esta propiedad tiene un valor de VARIANT TRUE, el descodificador de audio realiza un plegado de Lt-Rt (en matrices) hacia abajo en estéreo y, a continuación, se puede usar cualquier descodificador Dolby Surround para descodificar el envolvente con \_ matriz. Por ejemplo, el descodificador de audio podría realizar Lt-Rt doble hacia abajo en el contenido 5.1 o 7.1.

Esta propiedad solo se admite cuando el descodificador actúa como un objeto multimedia DirectX (DMO). No se admite ningún plegado de ningún tipo cuando el descodificador actúa como Media Foundation transform (MFT).

En Windows Vista, si obtiene una interfaz **IPropertyStore** en un descodificador de audio, el descodificador actúa como MFT. Por lo tanto, esta propiedad no se puede usar en Windows Vista. Para obtener información sobre cuándo un descodificador actúa como un DMO o un MFT, vea las páginas de referencia de códecs individuales en [Objetos de códec](codecobjects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
