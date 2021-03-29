---
description: Especifica el modo de control de división. Los valores válidos son 0, 1, y 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Propiedad CODECAPI_AVEncSliceControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000869"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>\_Propiedad AVEncSliceControlMode de CODECAPI

Especifica el modo de control de división. Los valores válidos son 0, 1, y 2.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valor de propiedad

Valores de modo de control de segmento:



| Value                                                                        | Significado                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Si se establece este valor en 0, se indica que la propiedad [ \_ AVEncSliceControlSize de CODECAPI](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de macrobloques por segmento.<br/>     |
| <dl> <dt>1</dt> </dl> | Si se establece este valor en 1, se indica que la propiedad [ \_ AVEncSliceControlSize de CODECAPI](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de bits por segmento.<br/>            |
| <dl> <dt>2</dt> </dl> | Si se establece este valor en 2, se indica que la propiedad [ \_ AVEncSliceControlSize de CODECAPI](codecapi-avencslicecontrolsize.md) especificará el tamaño del sector en unidades de adaptativo macrobloque filas por segmento.<br/> |



 

El codificador devuelve los valores que admite.

## <a name="remarks"></a>Observaciones

**Codificadores H. 264/AVC:**

Se recomienda que el codificador admita [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Si no se llama a [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) para CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) para CODECAPI \_ AVEncSliceControlMode puede devolver **VFW \_ E \_ CODECAPI \_ ningún \_ \_ valor actual**. [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) puede devolver **VFW \_ E \_ CODECAPI \_ no \_ default** para CODECAPI \_ AVEncSliceControlMode.

El valor predeterminado recomendado es 2 (tamaño en MB fila por segmento).

Se trata de una API estática, lo que significa que la aplicación ha logrado cambiar esto mientras el codificador se está ejecutando.

## <a name="examples"></a>Ejemplos


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

