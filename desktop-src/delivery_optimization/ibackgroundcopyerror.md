---
title: Interfaz IBackgroundCopyError (Deliveryoptimization. h)
description: Use la interfaz IBackgroundCopyError para determinar la causa de un error y si el proceso de transferencia puede continuar.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interfaz IBackgroundCopyError
- Interfaz IBackgroundCopyError, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490264"
---
# <a name="ibackgroundcopyerror-interface"></a>Interfaz IBackgroundCopyError

Use la interfaz **IBackgroundCopyError** para determinar la causa de un error y si el proceso de transferencia puede continuar.

Crea un objeto de error solo cuando el estado del trabajo es BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. No crea un objeto de error cuando se produce un error en un método de la interfaz **IBackgroundCopyXXXX** . El objeto de error está disponible hasta que comienza la transferencia de datos (el estado del trabajo cambia a BG_JOB_STATE_TRANSFERRING) del trabajo.

Para obtener un objeto **IBackgroundCopyError** , llame al método [**IBackgroundCopyJob:: GetError**](ibackgroundcopyjob-geterror.md) .

## <a name="members"></a>Miembros

La interfaz **IBackgroundCopyError** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyError** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBackgroundCopyError** tiene estos métodos.



| Método                                                   | Descripción                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Recupera el código de error e identifica el contexto en el que se produjo el error.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Recupera un puntero de interfaz al objeto de archivo asociado al error.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**IBackgroundCopyJob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

