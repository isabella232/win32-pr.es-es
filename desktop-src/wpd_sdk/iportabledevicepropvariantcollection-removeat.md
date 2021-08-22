---
description: 'Método IPortableDevicePropVariantCollection::RemoveAt: el método RemoveAt quita el elemento almacenado en la ubicación especificada por el índice especificado.'
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: Método IPortableDevicePropVariantCollection::RemoveAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 311b3511329ed15f5afd83d5a84c0c5abd62fe3f44000962fbdcd2f8ddd67c9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026903"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>IPortableDevicePropVariantCollection::RemoveAt (método)

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




