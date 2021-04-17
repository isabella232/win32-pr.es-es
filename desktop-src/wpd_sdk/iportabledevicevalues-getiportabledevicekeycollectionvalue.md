---
description: El método GetIPortableDeviceKeyCollectionValue recupera un valor de IPortableDeviceKeyCollection (tipo VT \_ desconocido) especificado por una clave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (método) (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680188"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (método)

El método **GetIPortableDeviceKeyCollectionValue** recupera un valor de **IPORTABLEDEVICEKEYCOLLECTION** (tipo VT \_ desconocido) especificado por una clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

Clave **REFPROPERTYKEY** que especifica el elemento que se va a recuperar.

</dd> <dt>

*ppValue* \[ enuncia\]
</dt> <dd>

Puntero al puntero de la interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) recuperada. El autor de la llamada es responsable de llamar a **Release** en la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                            | Descripción                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                   | El método se ha llevado a cabo de forma correcta.<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La propiedad especificada por *key* no es una interfaz **IPortableDeviceKeyCollection** .<br/> |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ no \_ encontrado)**</dt> </dl> | La propiedad especificada por la *clave* no está en la colección.<br/>                             |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [recuperar eventos de servicio admitidos](retrieving-supported-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Recuperación de eventos de servicio admitidos](retrieving-supported-events.md)
</dt> <dt>

[Recuperando métodos de servicio admitidos](retrieving-supported-methods.md)
</dt> </dl>

 

 




