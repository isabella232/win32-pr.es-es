---
description: El método GetCount recupera el número de elementos de la colección.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'IPortableDeviceValues:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650167"
---
# <a name="iportabledevicevaluesgetcount-method"></a>IPortableDeviceValues:: GetCount (método)

El método **getCount** recupera el número de elementos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcelt* \[ de\]
</dt> <dd>

Puntero a un **valor DWORD** que contiene el número de elementos de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> </dl>

 

 




