---
title: Mensaje de EM_GETHANDLE (Winuser. h)
description: Obtiene un identificador de la memoria asignada actualmente para el texto de un control de edición multilínea.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE controles de mensajes de Windows
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
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534684"
---
# <a name="em_gethandle-message"></a>\_Mensaje de GETHANDLE em

Obtiene un identificador de la memoria asignada actualmente para el texto de un control de edición multilínea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de memoria que identifica el búfer que contiene el contenido del control de edición. Si se produce un error, como el envío del mensaje a un control de edición de una sola línea, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Si la función se ejecuta correctamente, la aplicación puede tener acceso al contenido del control de edición convirtiendo el valor devuelto en [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) y pasándolo a [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock). **LocalLock** devuelve un puntero a un búfer que es una matriz terminada en NULL de **Char** s o **WCHAR** s, dependiendo de si una función ANSI o Unicode creó el control. Por ejemplo, si se usó [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , el búfer es una matriz de **Char** s, pero si se usó **CreateWindowExW** , el búfer es una matriz de **WCHAR** s. Es posible que la aplicación no cambie el contenido del búfer. Para desbloquear el búfer, la aplicación llama a [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) antes de permitir que el control de edición reciba mensajes nuevos.

> [!Note]  
> En el caso de Comctl32.dll versión 6, el búfer siempre contiene una matriz de **WCHAR** s, independientemente de si una función ANSI o Unicode creó el control de edición. Para obtener más información sobre las versiones de DLL, vea [versiones de control comunes](common-control-versions.md).

 

Si la aplicación no puede cumplir las restricciones impuestas por la función **\_ GETHANDLE**, utilice las funciones [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) y [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para copiar el contenido del control de edición en un búfer proporcionado por la aplicación.

**Edición enriquecida:** No se admite el mensaje de **\_ GETHANDLE em** . Los controles Rich Edit no almacenan texto como una matriz de caracteres simple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_SETHANDLE em**](em-sethandle.md)
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

 

