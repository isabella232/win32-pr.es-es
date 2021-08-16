---
description: Especifica si el descodificador debe realizar la Lt-Rt desplegable.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76d086fd0f57262d249784fcabc5a98e8a18668cf0697618f3fbbe5528a2cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713816"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>Propiedad MFPKEY \_ WMADEC \_ LTRTOUTPUT

Especifica si el descodificador debe realizar la Lt-Rt desplegable.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Si esta propiedad tiene un valor de VARIANT FALSE y la salida es estéreo, el descodificador de audio usa un \_ sencillo plegado del canal. Si esta propiedad tiene un valor de VARIANT TRUE, el descodificador de audio realiza un plegado de Lt-Rt (en matrices) hacia abajo en estéreo y, a continuación, se puede usar cualquier descodificador Dolby Surround para descodificar el envolvente con \_ matriz. Por ejemplo, el descodificador de audio podría Lt-Rt en el contenido 5.1 o 7.1.

Esta propiedad solo se admite cuando el descodificador actúa como un objeto multimedia DirectX (DMO). No se admite ningún plegado de ningún tipo cuando el descodificador actúa como Media Foundation transformación (MFT).

En Windows Vista, si obtiene una interfaz **IPropertyStore** en un descodificador de audio, el descodificador actúa como MFT. Por lo tanto, esta propiedad no se puede usar en Windows Vista. Para obtener información sobre cuándo un descodificador actúa como un DMO o un MFT, vea las páginas de referencia de códecs individuales en [Objetos de códec](codecobjects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
