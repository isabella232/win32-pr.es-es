---
title: Método GetDisplayName IBackgroundCopyJob (Deliveryoptimization. h)
description: Recupera el nombre para mostrar del trabajo. Normalmente, se usa el nombre para mostrar para identificar el trabajo en una interfaz de usuario.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (método)
- GetDisplayName (método), interfaz IBackgroundCopyJob
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
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996872"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>IBackgroundCopyJob:: GetDisplayName (método)

Recupera el nombre para mostrar del trabajo. Normalmente, se usa el nombre para mostrar para identificar el trabajo en una interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDisplayName* \[ enuncia\]
</dt> <dd>

Cadena terminada en null que contiene el nombre para mostrar que identifica el trabajo. Más de un trabajo puede tener el mismo nombre para mostrar. Llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppDisplayName* cuando termine.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                                  | Descripción                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | El nombre para mostrar se recuperó correctamente.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | El parámetro *ppDisplayName* no puede ser **null**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

