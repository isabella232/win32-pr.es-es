---
description: El método GetAd recupera un elemento de la colección mediante un índice basado en cero.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'IPortableDeviceValuesCollection:: GetAt (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708211"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection:: GetAt (método)

El método **GetAd** recupera un elemento de la colección mediante un índice basado en cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ de\]
</dt> <dd>

**DWORD** que especifica un índice basado en cero en la colección.

</dd> <dt>

*ppValues* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) de la colección. El autor de la llamada es responsable de llamar a **Release** en esta interfaz cuando se realiza con ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El índice de base cero que se pasó estaba fuera del intervalo.<br/>             |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Un argumento de puntero necesario era **null**.<br/>                             |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | La colección contiene un puntero **IPortableDeviceValues** **nulo** .<br/> |



 

## <a name="remarks"></a>Observaciones

Los cambios que se realicen en los valores de la interfaz recuperada se realizarán en la versión almacenada en la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




