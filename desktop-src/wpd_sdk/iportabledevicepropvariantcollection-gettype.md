---
description: El método GetType recupera el tipo de datos de los elementos de la colección.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: Método IPortableDevicePropVariantCollection::GetType (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266900"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>IPortableDevicePropVariantCollection::GetType (método)

El **método GetType** recupera el tipo de datos de los elementos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pvt* \[ out\]
</dt> <dd>

Valor de **enumeración VARTYPE del** SDK de plataforma que indica el tipo de datos de todos los elementos de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | Un argumento de puntero necesario era **NULL.**<br/> |



 

## <a name="remarks"></a>Observaciones

Todos los elementos almacenados en **IPortableDevicePropVariantCollection** son del mismo tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




