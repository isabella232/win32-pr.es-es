---
title: Método IBackgroundCopyFile GetProgress (Deliveryoptimization.h)
description: Recupera información sobre el progreso de la transferencia de archivos.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Método GetProgress
- Método GetProgress, interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, método GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7c5fe4a9fcfac86403fd7f4c330d437156e57179b3bf692f53bf3777399b9bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610505"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>IBackgroundCopyFile::GetProgress (método)

Recupera información sobre el progreso de la transferencia de archivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProgress* \[ out\]
</dt> <dd>

Estructura cuyos miembros indican el progreso de la transferencia de archivos. Para obtener más información sobre el tipo de información de progreso disponible, consulte [**la estructura BG_FILE_PROGRESS**](bg-file-progress.md) datos.

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
| IID<br/>                      | IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyJob::GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





