---
title: Método GetFile de IBackgroundCopyError (Deliveryoptimization.h)
description: Recupera un puntero de interfaz al objeto de archivo asociado al error.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Método GetFile
- Método GetFile, interfaz IBackgroundCopyError
- Interfaz IBackgroundCopyError, método GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbed5497bcebb3518c7f6a56646976cc01fbfebc501af4a08e861139311f4bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096715"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>IBackgroundCopyError::GetFile (método)

Recupera un puntero de interfaz al objeto de archivo asociado al error.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFile* \[ out\]
</dt> <dd>

Puntero [**de interfaz IBackgroundCopyFile**](ibackgroundcopyfile.md) cuyos métodos se usan para determinar los nombres de archivo locales y remotos asociados al error. El *parámetro ppFile* se establece en **NULL si** el error no está asociado al archivo local o remoto. Cuando haya terminado, libere *ppFile*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT.**



| Código devuelto                                                                                                | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>                   | Recuperó correctamente un puntero de interfaz al objeto de archivo.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | El error no está asociado a un archivo local o remoto. El *parámetro ppFile* se establece en **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





