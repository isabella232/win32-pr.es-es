---
description: Especifica el modo de control de segmento. Los valores válidos son 0, 1, y 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269308"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>Propiedad CODECAPI \_ AVEncSliceControlMode

Especifica el modo de control de segmento. Los valores válidos son 0, 1, y 2.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valor de propiedad

Valores de modo de control de segmento:



| Value                                                                        | Significado                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Establecer este valor en 0 indica que la propiedad [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de macrobloques por segmento.<br/>     |
| <dl> <dt>1</dt> </dl> | Establecer este valor en 1 indica que la propiedad [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de bits por segmento.<br/>            |
| <dl> <dt>2</dt> </dl> | Establecer este valor en 2 indica que la propiedad [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará el tamaño del segmento en unidades de filas de macrobloqueo por segmento.<br/> |



 

El codificador devuelve los valores que admite.

## <a name="remarks"></a>Observaciones

**Codificadores H.264/AVC:**

Se recomienda que el codificador admita [**GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Si no se llama a [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) para CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) para CODECAPI \_ AVEncSliceControlMode puede devolver **VFW \_ E \_ CODECAPI \_ NO CURRENT \_ \_ VALUE**. [**GetDefaultValue puede**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) devolver **VFW \_ E \_ CODECAPI NO \_ \_ DEFAULT** para CODECAPI \_ AVEncSliceControlMode.

El valor predeterminado recomendado es 2 (tamaño en mb fila por segmento).

Se trata de una API estática, lo que significa que la aplicación no cambiará esto mientras se ejecuta el codificador.

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
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

