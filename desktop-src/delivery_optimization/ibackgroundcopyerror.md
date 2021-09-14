---
title: Interfaz IBackgroundCopyError (Deliveryoptimization.h)
description: Use la interfaz IBackgroundCopyError para determinar la causa de un error y si el proceso de transferencia puede continuar.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- IBackgroundCopyError (interfaz)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174865"
---
# <a name="ibackgroundcopyerror-interface"></a>IBackgroundCopyError (interfaz)

Use la **interfaz IBackgroundCopyError** para determinar la causa de un error y si el proceso de transferencia puede continuar.

DO crea un objeto de error solo cuando el estado del trabajo es BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. DO no crea un objeto de error cuando se produce un error en un método de interfaz **IBackgroundCopyXXXX.** El objeto de error está disponible hasta que do comienza a transferir datos (el estado del trabajo cambia a BG_JOB_STATE_TRANSFERRING) para el trabajo.

Para obtener un **objeto IBackgroundCopyError,** llame al [**método IBackgroundCopyJob::GetError.**](ibackgroundcopyjob-geterror.md)

## <a name="members"></a>Members

La **interfaz IBackgroundCopyError** hereda de [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyError** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyError tiene** estos métodos.



| Método                                                   | Descripción                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Recupera el código de error e identifica el contexto en el que se produjo el error.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Recupera un puntero de interfaz al objeto de archivo asociado al error.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

