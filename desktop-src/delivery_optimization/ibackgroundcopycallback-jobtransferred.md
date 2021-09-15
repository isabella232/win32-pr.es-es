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
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566760"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>IBackgroundCopyCallback::JobTransferred (Método)

Optimización de distribución (DO) llama a la implementación del **método JobTransferred** cuando todos los archivos del trabajo se han transferido correctamente.

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

## <a name="remarks"></a>Observaciones

Normalmente, la implementación debe llamar al [**método IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) para confirmar que DO ha transferido correctamente los archivos. Los archivos de descarga y el archivo de respuesta no están disponibles en el cliente hasta que se llama al **método** Complete.

Si no llama al método [**Complete**](ibackgroundcopyjob-complete.md) o al método [**IBackgroundCopyJob::Cancel,**](ibackgroundcopyjob-cancel.md) DO cancela el trabajo después de 30 días y elimina los archivos incompletos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
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

 

 





