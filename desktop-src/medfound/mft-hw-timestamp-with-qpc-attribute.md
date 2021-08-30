---
description: Especifica si un origen de dispositivo de hardware usa la hora del sistema para las marcas de tiempo.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: MFT_HW_TIMESTAMP_WITH_QPC_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af0081c384af4e0fb36da10d87979c1e2d9ad0256f474581f1be3d9fce213cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012655"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a>Atributo MFT \_ HW \_ TIMESTAMP WITH \_ \_ QPC \_

Especifica si un origen de dispositivo de hardware usa la hora del sistema para las marcas de tiempo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE**, el origen del dispositivo usa la hora del sistema, como devuelve **QueryPerformanceCounter,** para las marcas de tiempo. De lo contrario, el origen del dispositivo usa el reloj del dispositivo. El valor predeterminado es **FALSE**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




