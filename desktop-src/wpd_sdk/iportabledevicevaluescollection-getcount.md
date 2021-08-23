---
description: 'Método IPortableDeviceValuesCollection::GetCount: el método GetCount recupera el número de elementos de la colección.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: Método IPortableDeviceValuesCollection::GetCount (PortableDeviceTypes.h)
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
ms.openlocfilehash: abf157a8a539d98c5b75826e4568df7c3209a0efc2dab49f6487250dd08ae391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707375"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>IPortableDeviceValuesCollection::GetCount (Método)

El **método GetCount** recupera el número de elementos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcElems* \[ En\]
</dt> <dd>

Puntero a un **DWORD** que contiene el número de **interfaces IPortableDeviceValues** de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | Un argumento de puntero necesario era **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceValuesCollection (Interfaz)**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




