---
title: Mensaje de ACM_OPEN (commctrl. h)
description: Abre un clip AVI y muestra su primer fotograma en un control Animation. Puede enviar este mensaje explícitamente o utilizar la macro de animación \_ Open o Animate \_ OpenEx. Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN controles de mensajes de Windows
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
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422049"
---
# <a name="acm_open-message"></a>\_Mensaje abierto de ACM

Abre un clip AVI y muestra su primer fotograma en un control Animation. Puede enviar este mensaje explícitamente o utilizar la macro de [**animación \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) o [**Animate \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[Versión 4,71](common-control-versions.md) y versiones posteriores. Identificador de instancia del módulo del que se debe cargar el recurso. Establezca este valor en **null** para que el control use el valor de hInstance que se usa para crear la ventana. Tenga en cuenta que si una DLL crea la ventana, el valor predeterminado de *wParam* es el valor de hInstance del archivo dll, no de la aplicación que llama al archivo dll.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a un búfer que contiene la ruta de acceso del archivo AVI o el nombre de un recurso AVI. Como alternativa, este parámetro puede constar del identificador de recursos AVI en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y cero en [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Para crear este valor, use la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . El control carga el recurso AVI desde el módulo especificado por el identificador de instancia que se ha pasado a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , a la [**animación de \_ creación**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) de macros o a la función de creación de cuadros de diálogo que creó el control. En la [versión 4,71](common-control-versions.md) y posteriores, el recurso se carga desde el módulo especificado por *wParam*. Un recurso AVI debe tener el tipo "AVI". Si este parámetro es **null**, el sistema cierra el archivo AVI que se abrió previamente para el control de animación especificado, si existe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

El archivo AVI o el recurso especificado por *lpszName* no debe contener audio.

Se recomienda usar la versión Unicode de este mensaje, ACM \_ OPENW.

Solo puede abrir clips AVI silenciosos. ACM \_ Open and [**Animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) FAIL si *lParam* especifica un clip AVI que contiene sonido.

Puede usar [**animar \_ cerrar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) para cerrar un archivo AVI o un recurso AVI que se abrió previamente para el control de animación especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **ACM \_ OPENW** (Unicode) y **ACM \_ opena** (ANSI)<br/>                         |



 

