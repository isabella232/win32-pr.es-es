---
description: El método GetAt recupera un valor de la colección mediante el índice de base cero proporcionado.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: Método IPortableDeviceValues::GetAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843036"
---
# <a name="iportabledevicevaluesgetat-method"></a>IPortableDeviceValues::GetAt (método)

El **método GetAt** recupera un valor de la colección mediante el índice de base cero proporcionado.

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

*index* \[ En\]
</dt> <dd>

DWORD **que** especifica un índice de base cero en la colección.

</dd> <dt>

*pKey* \[ in, out\]
</dt> <dd>

Puntero **PROPERTYKEY** opcional que recupera la clave del elemento especificado.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

**PROPVARIANT opcional** que recupera el valor del elemento especificado. El autor de la llamada debe liberar la memoria llamando **a PropVariantClear** cuando haya terminado con ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Se especificó un número de índice no válido.<br/> |



 

## <a name="remarks"></a>Comentarios

Si una propiedad indica un valor de tipo VT UNKNOWN, la propiedad será uno de los dispositivos portátiles de \_ Windows ([**IPortableDeviceKeyCollection,**](iportabledevicekeycollection.md) [**IPortableDeviceValuesCollection,**](iportabledevicevaluescollection.md) [**IPortableDeviceValues**](iportabledevicevalues.md) o [**IPortableDevicePropVariantCollection).**](iportabledevicepropvariantcollection.md) No se pueden devolver otras interfaces Windows dispositivos portátiles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




