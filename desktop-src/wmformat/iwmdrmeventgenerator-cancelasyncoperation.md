---
title: Método CancelAsyncOperation de IWMDRMEventGenerator (Wmdrmsdk.h)
description: El método CancelAsyncOperation cancela una operación asincrónica.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Formato multimedia de windows del método CancelAsyncOperation
- Método CancelAsyncOperation windows Media Format , interfaz IWMDRMEventGenerator
- IWMDRMEventGenerator interfaz windows Media Format , Método CancelAsyncOperation
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251462"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>IWMDRMEventGenerator::CancelAsyncOperation (método)

El **método CancelAsyncOperation** cancela una operación asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*kieCancelationCookie* \[ En\]
</dt> <dd>

Puntero a la cookie de cancelación que identifica la operación asincrónica que se va a cancelar. El método utilizado para iniciar la operación proporciona esta cookie.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMEventGenerator (interfaz)**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





