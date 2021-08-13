---
title: Método IBackgroundCopyJob EnumFiles (Deliveryoptimization.h)
description: Recupera un puntero de interfaz IEnumBackgroundCopyFiles que se usa para enumerar los archivos de un trabajo.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Método EnumFiles
- Método EnumFiles, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ecd27e1de8dfaa16d7f5d2dc3218d3c993148a0878976e329b4953cefdc4c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543021"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>IBackgroundCopyJob::EnumFiles (método)

Recupera un puntero [**de interfaz IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que se usa para enumerar los archivos de un trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumFiles* \[ out\]
</dt> <dd>

[**Puntero de interfaz IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que se usa para enumerar los archivos del trabajo. Libere *ppEnumFiles* cuando haya terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** correcto o uno de los valores **HRESULT COM** estándar en caso de error.

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
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





