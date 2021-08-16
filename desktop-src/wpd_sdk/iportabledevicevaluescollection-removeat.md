---
description: 'Método IPortableDeviceValuesCollection::RemoveAt: el método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: Método IPortableDeviceValuesCollection::RemoveAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2796fd44016854d03322b8dfa0a11ce85d1afce16b9ae17cae02a6fc53804f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963554"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a>IPortableDeviceValuesCollection::RemoveAt (Método)

El **método RemoveAt** quita el elemento almacenado en la ubicación especificada por el índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Especifica el índice del elemento que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El índice especificado estaba fuera del intervalo.<br/> |



 

## <a name="remarks"></a>Comentarios

Debe especificar un índice de base cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValuesCollection (Interfaz)**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




