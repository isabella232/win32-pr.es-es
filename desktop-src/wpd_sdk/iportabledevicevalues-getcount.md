---
description: 'Método IPortableDeviceValues::GetCount: el método GetCount recupera el número de elementos de la colección.'
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: Método IPortableDeviceValues::GetCount (PortableDeviceTypes.h)
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
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086243"
---
# <a name="iportabledevicevaluesgetcount-method"></a>IPortableDeviceValues::GetCount (método)

El **método GetCount** recupera el número de elementos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcelt* \[ En\]
</dt> <dd>

Puntero a un **DWORD** que contiene el número de elementos de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> </dl>

 

 




