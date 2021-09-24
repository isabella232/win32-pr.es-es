---
title: Método JobModification de IBackgroundCopyCallback (Deliveryoptimization.h)
description: Optimización de distribución llama a la implementación del método JobModification cuando se ha modificado el trabajo.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Método JobModification
- Método JobModification, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 275e0ebe780a85a919e7c7692739273048e1fb85
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521352"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>IBackgroundCopyCallback::JobModification (método)

Optimización de distribución llama a la implementación del [**método JobModification**](https://www.bing.com/search?q=**JobModification**) cuando se ha modificado el trabajo. El servicio genera este evento cuando se transfieren bytes, se han agregado archivos al trabajo, se han modificado las propiedades o se ha cambiado el estado del trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJob* \[ En\]
</dt> <dd>

Contiene los métodos para acceder a la información de propiedad, progreso y estado del trabajo. No liberar *pJob*; Optimización de distribución libera la interfaz cuando devuelve [**el método JobModification.**](https://www.bing.com/search?q=**JobModification**)

</dd> <dt>

*dwReserved* \[ En\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver S_OK.

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

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





