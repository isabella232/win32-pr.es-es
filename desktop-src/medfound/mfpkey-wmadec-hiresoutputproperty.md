---
description: Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Propiedad MFPKEY_WMADEC_HIRESOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706131"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>\_ \_ Propiedad HIRESOUTPUT de MFPKEY WMADEC

Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACHiResOutput

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ false**

## <a name="remarks"></a>Observaciones

Establezca esta propiedad en VARIANT \_ true para descodificar el contenido de audio multicanal o de 24 bits, o audio con una velocidad de muestra superior a 48.000 Hz. Si el contenido se codifica en alta resolución, pero esta propiedad es \_ la variante falsa, se aplican los comportamientos siguientes:

-   La salida de DMO se limitará a un estéreo de 16 bits 48-KHz.
-   La MFT enumerará los modos de salida que están limitados a 16 bits y no implican cambios en el número de canales o la frecuencia de muestreo.

Las propiedades de audio de alta resolución se pasan en una estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , no en [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).

La salida de alta resolución solo está disponible si el descodificador se ejecuta en Windows XP o posterior. Puede establecer esta propiedad independientemente del sistema operativo en el que se ejecuta la aplicación. En las versiones de Windows anteriores a Windows XP, el descodificador omitirá esta configuración y entregará la salida estándar.

Muchos jugadores (incluidos Windows Media Player series 9 y versiones posteriores) establecen este valor para todo el contenido.

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

 

 
