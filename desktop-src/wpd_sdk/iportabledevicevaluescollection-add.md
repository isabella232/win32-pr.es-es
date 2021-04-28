---
description: 'Método IPortableDeviceValuesCollection::Add: el método Add agrega un elemento a la colección.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: IPortableDeviceValuesCollection::Add (método, PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083257"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>IPortableDeviceValuesCollection::Add (Método)

El **método Add** agrega un elemento a la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pValues* \[ En\]
</dt> <dd>

Puntero a una **interfaz IPortableDeviceValues** que se agregará a la colección. La interfaz no se copia realmente, pero se llama a **AddRef** en ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT.** Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria disponible para agregar el valor a la colección.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValuesCollection (Interfaz)**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




