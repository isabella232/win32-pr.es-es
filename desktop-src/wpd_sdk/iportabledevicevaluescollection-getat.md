---
description: 'Método IPortableDeviceValuesCollection::GetAt: el método GetAt recupera un elemento de la colección mediante un índice de base cero.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: Método IPortableDeviceValuesCollection::GetAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083263"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection::GetAt (método)

El **método GetAt** recupera un elemento de la colección mediante un índice de base cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ En\]
</dt> <dd>

**DWORD** que especifica un índice de base cero en la colección.

</dd> <dt>

*ppValues* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) de la colección. El autor de la llamada es responsable de **llamar a Release** en esta interfaz cuando haya terminado con ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT.** Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El índice de base cero que se pasó estaba fuera del intervalo.<br/>             |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | Un argumento de puntero necesario era **NULL.**<br/>                             |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | La colección contiene un **puntero NULL** **IPortableDeviceValues.**<br/> |



 

## <a name="remarks"></a>Comentarios

Los cambios realizados en los valores de la interfaz recuperada se realizarán en la versión almacenada en la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValuesCollection (Interfaz)**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




