---
title: Método IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: La optimización de entrega (DO) llama a la implementación del método JobError cuando el estado del trabajo cambia a BG_JOB_STATE_ERROR.
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
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422242"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>IBackgroundCopyCallback:: JobError (método)

La optimización de entrega (DO) llama a la implementación del método [**JobError**](https://www.bing.com/search?q=**JobError**) cuando el estado del trabajo cambia a BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJob* \[ de\]
</dt> <dd>

Contiene información relacionada con el trabajo, como el número de bytes y archivos transferidos antes de que se produjera el error. También contiene los métodos para reanudar y cancelar el trabajo. No libere *pJob*; Libera la interfaz cuando el método [**JobError**](https://www.bing.com/search?q=**JobError**) devuelve.

</dd> <dt>

*perror* \[ de\]
</dt> <dd>

Contiene información de error, como el archivo que se está procesando en el momento en que se produjo el error irrecuperable y una descripción del error. No liberar el *perror*; Libera la interfaz cuando el método [**JobError**](https://www.bing.com/search?q=**JobError**) devuelve.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver **S_OK**; de lo contrario, sigue llamando a este método hasta que se devuelva **S_OK** . Por motivos de rendimiento, debe limitar el número de veces que se devuelve un valor distinto de **S_OK** a varias veces. Como alternativa a la devolución de un código de error, considere la posibilidad de devolver siempre **S_OK** y de controlar el error internamente. El intervalo en el que se llama a este método es arbitrario.

## <a name="remarks"></a>Observaciones

Después de determinar la causa del error, realice una de las siguientes opciones:

-   Para cancelar el trabajo, llame al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) .
-   Para aceptar la parte del trabajo que se transfirió correctamente antes de que se produjera el error, llame al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) . Esta opción no se aplica a los trabajos de carga; no se puede completar una parte de un trabajo de carga.
-   Para finalizar el procesamiento del trabajo, corrija el problema y, a continuación, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) .

Los errores transitorios no generan llamadas al método [**JobError**](https://www.bing.com/search?q=**JobError**) .

Devuelve BG_ERROR_CONTEXT_REMOTE_FILE si el trabajo ha alcanzado un error HTTP 403, BG_ERROR_CONTEXT_NONE de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





