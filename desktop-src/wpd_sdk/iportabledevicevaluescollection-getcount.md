---
description: El método GetCount recupera el número de elementos de la colección.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'IPortableDeviceValuesCollection:: GetCount (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718629"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>IPortableDeviceValuesCollection:: GetCount (método)

El método **getCount** recupera el número de elementos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcElems* \[ de\]
</dt> <dd>

Puntero a un **valor DWORD** que contiene el número de interfaces **IPortableDeviceValues** de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**\_puntero E**</dt> </dl> | Un argumento de puntero necesario era **null**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




