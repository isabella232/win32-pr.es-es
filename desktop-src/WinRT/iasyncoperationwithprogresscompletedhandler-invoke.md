---
description: Invoca el método al que se llama cuando la operación asincrónica especificada informa del progreso.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke (método)'
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
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154305"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke (método)

Invoca el método al que se llama cuando la operación asincrónica especificada informa del progreso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*asyncInfo* \[ de\]
</dt> <dd>

Tipo: **[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _

La acción asincrónica que informa de la finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
