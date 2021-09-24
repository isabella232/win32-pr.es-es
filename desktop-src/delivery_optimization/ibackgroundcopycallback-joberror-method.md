---
title: Método IBackgroundCopyCallback JobError (Deliveryoptimization.h)
description: Optimización de distribución llama a la implementación del método JobError cuando el estado del trabajo cambia a BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Método JobError
- Método JobError, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 434af6a2e64cae16b0b6605c6b3d426d9c37736b
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520226"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>IBackgroundCopyCallback::JobError (método)

Optimización de distribución llama a la implementación del [**método JobError**](https://www.bing.com/search?q=**JobError**) cuando el estado del trabajo cambia a BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJob* \[ En\]
</dt> <dd>

Contiene información relacionada con el trabajo, como el número de bytes y archivos transferidos antes de que se produjese el error. También contiene los métodos para reanudar y cancelar el trabajo. No liberar *pJob*; Optimización de distribución libera la interfaz cuando devuelve [**el método JobError.**](https://www.bing.com/search?q=**JobError**)

</dd> <dt>

*pError* \[ En\]
</dt> <dd>

Contiene información de error, como el archivo que se está procesando en el momento en que se produjo el error grave y una descripción del error. No liberar *pError*; Optimización de distribución libera la interfaz cuando se devuelve [**el método JobError.**](https://www.bing.com/search?q=**JobError**)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver **S_OK**; De lo contrario, Optimización de distribución a este método hasta **que S_OK** se devuelve. Por motivos de rendimiento, debe limitar el número de veces que devuelve un valor distinto de **S_OK** varias veces. Como alternativa a devolver un código de error, considere la posibilidad de devolver **siempre S_OK** control del error internamente. El intervalo en el que se llama a este método es arbitrario.

## <a name="remarks"></a>Comentarios

Después de determinar la causa del error, realice una de las siguientes opciones:

-   Para cancelar el trabajo, llame al [**método IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)
-   Para aceptar la parte del trabajo que se transfirieron correctamente antes de que se produjese el error, llame al [**método IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md) Esta opción no se aplica a los trabajos de carga; no puede completar una parte de un trabajo de carga.
-   Para finalizar el procesamiento del trabajo, corrija el problema y, a continuación, llame al [**método IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md)

Los errores transitorios no generan llamadas al [**método JobError.**](https://www.bing.com/search?q=**JobError**)

Optimización de distribución devuelve BG_ERROR_CONTEXT_REMOTE_FILE si el trabajo ha producido un error HTTP 403, BG_ERROR_CONTEXT_NONE lo contrario.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





