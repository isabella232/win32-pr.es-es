---
description: El método Clear libera y, a continuación, quita todos los elementos de la colección. La colección se considera vacía después de llamar a este método.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: Método IPortableDevicePropVariantCollection::Clear (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0cec3f12757fe43c408488204de8b0dd95d5e95c75d8315ea758e4311ff5e9bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194143"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>IPortableDevicePropVariantCollection::Clear (Método)

El **método Clear** libera y, a continuación, quita todos los elementos de la colección. La colección se considera vacía después de llamar a este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Después de **llamar a Clear**, la colección se considera sin tipo, lo que significa que vartype en el que se estableció anteriormente ya no restringe las operaciones **de** adición. Una llamada a **Add después** de llamar **a Clear** se considera la "primera" **agregar** para esta colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




