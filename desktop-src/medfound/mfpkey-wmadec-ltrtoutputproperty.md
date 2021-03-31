---
description: Especifica si el descodificador debe realizar Lt-Rt pliegue.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Propiedad MFPKEY_WMADEC_LTRTOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155388"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>\_ \_ Propiedad LTRTOUTPUT de MFPKEY WMADEC

Especifica si el descodificador debe realizar Lt-Rt pliegue.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ false**

## <a name="remarks"></a>Observaciones

Si esta propiedad tiene un valor de VARIANT \_ false y el resultado es estéreo, el descodificador de audio usa un simple plegado de canal. Si esta propiedad tiene un valor de VARIANT \_ true, el descodificador de audio realiza Lt-Rt (matriz) en estéreo y, a continuación, se puede usar cualquier descodificador Dolby Surround para descodificar el código envolvente de matriz. Por ejemplo, el descodificador de audio podría realizar Lt-Rt desplegar en el contenido 5,1 o 7,1.

Esta propiedad solo se admite cuando el descodificador actúa como un objeto multimedia de DirectX (DMO). No se admite la displiegue de ningún tipo cuando el descodificador actúa como una transformación de Media Foundation (MFT).

En Windows Vista, si obtiene una interfaz **IPropertyStore** en un descodificador de audio, el descodificador actúa como MFT. Por consiguiente, esta propiedad no se puede usar en Windows Vista. Para obtener información sobre cuándo un descodificador actúa como DMO o MFT, consulte las páginas de referencia de códecs individuales en [objetos de códec](codecobjects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
