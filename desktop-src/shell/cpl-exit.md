---
description: Se envía una vez a la función CPlApplet de una Panel de control antes de que se libera el archivo DLL que Panel de control aplicación.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: CPL_EXIT mensaje (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9007c05de134b32e3c4dfd7b256f2392f547d298b2d654dddc256b6ed711bb9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715607"
---
# <a name="cpl_exit-message"></a>Mensaje exit de CPL \_

Se envía una vez a [**la función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una Panel de control antes de que se haya publicado el archivo DLL Panel de control aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Comentarios

Este mensaje se envía después de enviar el último mensaje STOP de [**CPL. \_**](cpl-stop.md)

En respuesta a este mensaje, una Panel de control debe liberar toda la memoria que haya asignado y realizar una limpieza de nivel global.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
