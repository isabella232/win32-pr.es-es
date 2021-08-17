---
description: El método GetIPortableDeviceKeyCollectionValue recupera un valor IPortableDeviceKeyCollection (tipo VT \_ UNKNOWN) especificado por una clave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: Método IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 13a7ccde6a7cf5a73c78cc382341f7d750d9032cbfd8d69bdcfd3e318eeccece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194106"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>Método IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue

El **método GetIPortableDeviceKeyCollectionValue** recupera un valor **IPortableDeviceKeyCollection** (tipo VT \_ UNKNOWN) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se recuperará.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Puntero al puntero de interfaz [**IPortableDeviceKeyCollection recuperado.**](iportabledevicekeycollection.md) El autor de la llamada es responsable de **llamar a Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key no* es una **interfaz IPortableDeviceKeyCollection.**<br/> |
| <dl> <dt>**HRESULT \_ DE \_ WIN32(ERROR \_ NO \_ ENCONTRADO)**</dt> </dl> | La propiedad especificada por *key no* está en la colección.<br/>                             |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Recuperación de eventos de servicio admitidos.](retrieving-supported-events.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperar métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> </dl>

 

 




