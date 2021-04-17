---
title: Método IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: El método CancelAsyncOperation cancela una operación asincrónica.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Método CancelAsyncOperation formato de Windows Media
- Método CancelAsyncOperation formato de Windows Media, interfaz IWMDRMEventGenerator
- Interfaz IWMDRMEventGenerator formato de Windows Media, método CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660651"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>IWMDRMEventGenerator:: CancelAsyncOperation (método)

El método **CancelAsyncOperation** cancela una operación asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*punkCancelationCookie* \[ de\]
</dt> <dd>

Puntero a la cookie de cancelación que identifica la operación asincrónica que se va a cancelar. Esta cookie la proporciona el método que se usa para iniciar la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





