---
title: EM_GETHANDLE mensaje (Winuser.h)
description: Obtiene un identificador de la memoria asignada actualmente para el texto de un control de edición multilínea.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09ade5545197df2dbc9310b708cd7521334bba68f41a14329dd865e84fdee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019653"
---
# <a name="em_gethandle-message"></a>Mensaje \_ GETHANDLE DE EM

Obtiene un identificador de la memoria asignada actualmente para el texto de un control de edición multilínea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de memoria que identifica el búfer que contiene el contenido del control de edición. Si se produce un error, como el envío del mensaje a un control de edición de una sola línea, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Si la función se realiza correctamente, la aplicación puede tener acceso al contenido del control de edición al convertir el valor devuelto en [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) y pasarlo a [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock). **LocalLock** devuelve un puntero a un búfer que es una matriz terminada en NULL de **CHAR** s o **WCHAR** s, en función de si una función ANSI o Unicode creó el control. Por ejemplo, si se [**usó CreateWindowExA,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) el búfer es una matriz de **CHAR,** pero si se usó **CreateWindowExW,** el búfer es una matriz de **WCHAR.** Es posible que la aplicación no cambie el contenido del búfer. Para desbloquear el búfer, la aplicación llama a [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) antes de permitir que el control de edición reciba nuevos mensajes.

> [!Note]  
> Para Comctl32.dll versión 6, el búfer siempre contiene una matriz de **WCHAR,** independientemente de si una función ANSI o Unicode creó el control de edición. Para obtener más información sobre las versiones de DLL, vea [Versiones de control comunes](common-control-versions.md).

 

Si la aplicación no puede cumplir las restricciones impuestas por **EM \_ GETHANDLE,** use las funciones [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) y [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para copiar el contenido del control de edición en un búfer proporcionado por la aplicación.

**Edición enriquecte:** No se admite el mensaje **EM \_ GETHANDLE.** Los controles de edición enriquecciones no almacenan texto como una matriz simple de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

