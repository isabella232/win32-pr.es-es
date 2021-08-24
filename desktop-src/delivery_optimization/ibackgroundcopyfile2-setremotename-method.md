---
title: Método IBackgroundCopyFile2 SetRemoteName (Deliveryoptimization.h)
description: Cambia el nombre remoto a una nueva dirección URL en un trabajo de descarga.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Método SetRemoteName
- Método SetRemoteName, interfaz IBackgroundCopyFile2
- Interfaz IBackgroundCopyFile2, método SetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4a2ed93a264aa12d61291c3562a455a026e0dfd0d727648b7d13f6ffe360015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636025"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>IBackgroundCopyFile2::SetRemoteName (método)

Cambia el nombre remoto a una nueva dirección URL en un trabajo de descarga.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RemoteName* \[ En\]
</dt> <dd>

Cadena terminada en NULL que contiene el nombre del archivo en el servidor. Para obtener información sobre cómo especificar el nombre remoto, vea el **miembro RemoteName.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos, así como otros.



| Código devuelto                                                                                  | Descripción                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>     | Success<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | El nuevo nombre remoto es una dirección URL no válida o la nueva dirección URL es demasiado larga (la dirección URL no puede superar los 2200 caracteres).<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama a este método si desea cambiar la dirección URL utilizada para transferir el archivo o si desea cambiar el nombre de archivo o la ruta de acceso.

Este método no serializa cuando devuelve . Para serializar el cambio, [**suspenda**](ibackgroundcopyjob-suspend.md) el trabajo, llame a este método (si cambia varios archivos en el trabajo, use un bucle) y [**reanude**](ibackgroundcopyjob-resume.md) el trabajo. Llamar al **método IBackgroundCopyJob::Resume** serializa el cambio.

Si la marca de tiempo o el tamaño de archivo del nuevo nombre remoto son diferentes del nombre remoto anterior o el nuevo servidor no admite la reanudación del punto de comprobación (para los nombres remotos HTTP), DO reinicia la descarga. De lo contrario, la transferencia se reanuda desde la misma posición en el nuevo servidor. DO no reinicia los archivos ya transferidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 se define como 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





