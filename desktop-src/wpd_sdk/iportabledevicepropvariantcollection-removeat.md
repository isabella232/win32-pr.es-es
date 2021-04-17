---
description: El método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'IPortableDevicePropVariantCollection:: RemoveAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699406"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>IPortableDevicePropVariantCollection:: RemoveAt (método)

El método **RemoveAt** quita el elemento almacenado en la ubicación especificada por el índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Especifica el índice del elemento que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El índice especificado estaba fuera del intervalo.<br/> |



 

## <a name="remarks"></a>Observaciones

Debe especificar un índice basado en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




