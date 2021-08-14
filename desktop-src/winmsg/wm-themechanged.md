---
description: Difusión a cada ventana después de un evento de cambio de tema. Algunos ejemplos de eventos de cambio de tema son la activación de un tema, la desactivación de un tema o una transición de un tema a otro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: WM_THEMECHANGED mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b070cb492fa5db94acb97cd07f3de87455189d542aaaad2a51a3e0ecc6b4268d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199914"
---
# <a name="wm_themechanged-message"></a>Mensaje \_ THEMECHANGED de WM

Difusión a cada ventana después de un evento de cambio de tema. Algunos ejemplos de eventos de cambio de tema son la activación de un tema, la desactivación de un tema o una transición de un tema a otro.


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro está reservado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro está reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> El sistema operativo publica este mensaje. Normalmente, las aplicaciones no envían este mensaje.

 

Los temas son especificaciones para la apariencia de los controles, por lo que el elemento visual de un control se trata por separado de su funcionalidad.

Para liberar un identificador de tema existente, llame [**a CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata). Para adquirir un nuevo identificador de tema, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

Después de la **difusión DE WM \_ THEMECHANGED,** los identificadores de tema existentes no son válidos. Una ventana que tenga en cuenta el tema debe liberar y volver a abrir cualquiera de sus identificadores de tema preexisteros cuando recibe el **mensaje \_ THEMECHANGED de WM.** Si la [**función OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) devuelve **NULL,** la ventana debe pintar sin llamar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
