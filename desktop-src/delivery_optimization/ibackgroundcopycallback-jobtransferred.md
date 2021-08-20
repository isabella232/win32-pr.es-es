---
title: Método IBackgroundCopyCallback JobTransferred (Deliveryoptimization.h)
description: Optimización de distribución (DO) llama a la implementación del método JobTransferred cuando todos los archivos del trabajo se han transferido correctamente.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Método JobTransferred
- Método JobTransferred, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69cf1a739e15bc7341769bdc01549ad439a1c93877f653f0689e686eb8bac1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047103"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>IBackgroundCopyCallback::JobTransferred (Método)

Optimización de distribución (DO) llama a la implementación del método **JobTransferred** cuando todos los archivos del trabajo se han transferido correctamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJob* \[ En\]
</dt> <dd>

Contiene información relacionada con el trabajo, como la hora en que se completó el trabajo, el número de bytes transferidos y el número de archivos transferidos. No liberar *pJob*; DO libera la interfaz cuando se devuelve el método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver S_OK.

## <a name="remarks"></a>Comentarios

Normalmente, la implementación debe llamar al [**método IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) para confirmar que DO ha transferido correctamente los archivos. Los archivos de descarga y el archivo de respuesta no están disponibles en el cliente hasta que se llama al **método** Complete.

Si no llama al método [**Complete**](ibackgroundcopyjob-complete.md) o al método [**IBackgroundCopyJob::Cancel,**](ibackgroundcopyjob-cancel.md) DO cancela el trabajo después de 30 días y elimina los archivos incompletos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





