---
title: ACM_OPEN mensaje (Commctrl.h)
description: Abre un clip AVI y muestra su primer fotograma en un control de animación. Puede enviar este mensaje explícitamente o usar la macro Animar \_ Open o Animar \_ OpenEx. Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN controles de Windows mensaje
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5af2bd996af159217c92d78102a97e5c530d34cf445d5ad34186cecb93ab85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922175"
---
# <a name="acm_open-message"></a>Mensaje OPEN de ACM \_

Abre un clip AVI y muestra su primer fotograma en un control de animación. Puede enviar este mensaje explícitamente o usar la macro [**Animar \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) [**o Animar \_ OpenEx.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[Versión 4.71](common-control-versions.md) y posteriores. Identificador de instancia del módulo desde el que se debe cargar el recurso. Establezca este valor en **NULL para** que el control use el valor HINSTANCE usado para crear la ventana. Tenga en cuenta que si la ventana se crea mediante un archivo DLL, el valor predeterminado de *wParam* es el valor HINSTANCE del archivo DLL, no de la aplicación que llama al archivo DLL.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que contiene la ruta de acceso del archivo AVI o el nombre de un recurso AVI. Como alternativa, este parámetro puede constar del identificador de recurso AVI en [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y cero en [**HIWORD.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Para crear este valor, use la [**macro MAKEINTRESOURCE.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) El control carga el recurso AVI desde el módulo especificado por el identificador de instancia pasado a la función [**CreateWindow,**](/windows/desktop/api/winuser/nf-winuser-createwindowa) la macro [**Animate \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) o la función de creación del cuadro de diálogo que creó el control. En [la versión 4.71](common-control-versions.md) y posteriores, el recurso se carga desde el módulo especificado por *wParam*. Un recurso AVI debe tener el tipo "AVI". Si este parámetro es **NULL,** el sistema cierra el archivo AVI que se abrió previamente para el control de animación especificado, si existe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

El archivo o recurso AVI especificado por *lpszName* no debe contener audio.

Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.

Solo puede abrir clips AVI silenciosos. ACM \_ OPEN y Animate [**\_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) producirán un error *si lParam* especifica un clip AVI que contiene sonido.

Puede usar [**Animar \_ cerrar para**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) cerrar un archivo AVI o un recurso AVI que se abrió previamente para el control de animación especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **ACM \_ OPENW** (Unicode) y **ACM \_ OPENA** (ANSI)<br/>                         |



 

