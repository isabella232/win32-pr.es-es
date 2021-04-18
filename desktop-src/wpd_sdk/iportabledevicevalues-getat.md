---
description: El método GetAd recupera un valor de la colección utilizando el índice de base cero proporcionado.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'IPortableDeviceValues:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649881"
---
# <a name="iportabledevicevaluesgetat-method"></a>IPortableDeviceValues:: GetAt (método)

El método **GetAd** recupera un valor de la colección utilizando el índice de base cero proporcionado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**DWORD** que especifica un índice basado en cero en la colección.

</dd> <dt>

*pKey* \[ in, out\]
</dt> <dd>

Un puntero **PROPERTYKEY** opcional que recupera la clave del elemento especificado.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

**PROPVARIANT** opcional que recupera el valor del elemento especificado. El autor de la llamada debe liberar la memoria mediante una llamada a **PropVariantClear** cuando se realiza con ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Se ha especificado un número de índice no válido.<br/> |



 

## <a name="remarks"></a>Observaciones

Si una propiedad indica un valor de tipo VT \_ Unknown, la propiedad será uno de los dispositivos portátiles de Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) o [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Los dispositivos portátiles de Windows no pueden devolver otras interfaces.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




