---
title: Método IBackgroundCopyJob GetDisplayName (Deliveryoptimization.h)
description: Recupera el nombre para mostrar del trabajo. Normalmente, se usa el nombre para mostrar para identificar el trabajo en una interfaz de usuario.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (método)
- Método GetDisplayName, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetDisplayName
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a50d2bdc1c492725b79368774f07755c7b629d73209a7d53f865cc738eb7025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755545"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>IBackgroundCopyJob::GetDisplayName (método)

Recupera el nombre para mostrar del trabajo. Normalmente, se usa el nombre para mostrar para identificar el trabajo en una interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDisplayName* \[ out\]
</dt> <dd>

Cadena terminada en NULL que contiene el nombre para mostrar que identifica el trabajo. Más de un trabajo puede tener el mismo nombre para mostrar. Llame a [**la función CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppDisplayName* cuando haya terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                                  | Descripción                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>     | El nombre para mostrar se recuperó correctamente.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | El *parámetro ppDisplayName* no puede ser **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

