---
description: Especifica si el codificador utiliza la codificación de velocidad de bits variable (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Propiedad MFPKEY_VBRENABLED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908746"
---
# <a name="mfpkey_vbrenabled-property"></a>\_Propiedad VBRENABLED de MFPKEY

Especifica si el codificador utiliza la codificación de velocidad de bits variable (VBR). Lectura y escritura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ false**

## <a name="remarks"></a>Observaciones

Este valor debe establecerse en **Variant \_ true** para cualquiera de las demás propiedades de VBR que va a usar el códec.

Después de establecer este valor en **Variant \_ true** en el codificador de audio, los tipos de salida que se recuperan mediante el método [**IMediaObject:: GETOUTPUTTYPE**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) son tipos de VBR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MFPKEY \_ restricción de \_ VBRQUALITY enumerada \_**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**MFPKEY \_ deseado \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
