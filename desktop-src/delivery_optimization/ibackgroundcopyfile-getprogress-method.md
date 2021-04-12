---
title: Método IBackgroundCopyFile GetProgress (Deliveryoptimization. h)
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
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490265"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>IBackgroundCopyFile:: GetProgress (método)

Recupera información sobre el progreso de la transferencia de archivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProgress* \[ enuncia\]
</dt> <dd>

Estructura cuyos miembros indican el progreso de la transferencia de archivos. Para obtener más información sobre el tipo de información de progreso disponible, vea la estructura [**BG_FILE_PROGRESS**](bg-file-progress.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyJob:: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





