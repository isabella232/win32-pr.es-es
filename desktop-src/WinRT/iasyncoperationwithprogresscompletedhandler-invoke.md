---
description: Invoca el método al que se llama cuando la operación asincrónica especificada notifica el progreso.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 141f79398e1f9f250b402df130daa728c8e2f0e5f78702d7866dbe9a202b5978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323124"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke (Método)

Invoca el método al que se llama cuando la operación asincrónica especificada notifica el progreso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*asyncInfo* \[ En\]
</dt> <dd>

Tipo: **[ **IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\***

Acción asincrónica que informa de la finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
