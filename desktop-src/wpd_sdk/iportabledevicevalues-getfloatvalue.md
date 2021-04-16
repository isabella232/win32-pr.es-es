---
description: El método GetFloatValue recupera un valor FLOAT (tipo VT \_ R4) especificado por una clave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'IPortableDeviceValues:: GetFloatValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649788"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>IPortableDeviceValues:: GetFloatValue (método)

El método **GetFloatValue** recupera un valor **float** (tipo VT \_ R4) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.

</dd> <dt>

*pValue* \[ enuncia\]
</dt> <dd>

Puntero al valor de **punto flotante** recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                             | Descripción                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | El método se ha llevado a cabo de forma correcta.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>    | La propiedad especificada por *key* no es un tipo **float** .<br/>  |
| <dl> <dt>**E \_ \_ ID. de prop \_ no compatible**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetFloatValue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




