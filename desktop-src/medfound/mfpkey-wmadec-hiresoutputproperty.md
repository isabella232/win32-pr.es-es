---
description: Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468617"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>Propiedad MFPKEY \_ WMADEC \_ HIRESOUTPUT

Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACHiResOutput

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Observaciones

Establezca esta propiedad en VARIANT TRUE para descodificar contenido de audio multicanal o de 24 bits, o audio con una velocidad de muestreo superior \_ a 48 000 Hz. Si el contenido está codificado en alta resolución, pero esta propiedad es VARIANT \_ FALSE, se aplican los comportamientos siguientes:

-   La DMO salida se limitará a estéreo de 16 bits y 48 KHz.
-   MFT enumerará los modos de salida que están limitados a 16 bits y que no implican cambios en el recuento de canales o la frecuencia de muestreo.

Las propiedades del audio de alta resolución se pasan en una [**estructura DE FORMAENTEXTENSIBLE,**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) no [**EN FORMA DE ONDAATEX.**](/previous-versions/dd757713(v=vs.85))

La salida de alta resolución solo está disponible si el descodificador se ejecuta Windows XP o posterior. Puede establecer esta propiedad independientemente del sistema operativo en el que se ejecute la aplicación. En las versiones de Windows anteriores a Windows XP, el descodificador omitirá esta configuración y entregará la salida estándar.

Muchos reproductores (incluidos Reproductor de Windows Media serie 9 y versiones posteriores) establecen este valor para todo el contenido.

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

 

 
