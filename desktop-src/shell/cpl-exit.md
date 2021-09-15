---
description: Se envía una vez a la función CPlApplet de una Panel de control antes de que se libera el archivo DLL que Panel de control aplicación.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: CPL_EXIT mensaje (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468290"
---
# <a name="cpl_exit-message"></a>Mensaje EXIT de CPL \_

Se envía una vez a la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una Panel de control antes de que se libera el archivo DLL que Panel de control aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Observaciones

Este mensaje se envía después de enviar el último mensaje STOP de [**CPL. \_**](cpl-stop.md)

En respuesta a este mensaje, una Panel de control debe liberar toda la memoria que haya asignado y realizar una limpieza de nivel global.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
