---
description: Difundir a cada ventana después de un evento de cambio de tema. Algunos ejemplos de eventos de cambio de tema son la activación de un tema, la desactivación de un tema o una transición de un tema a otro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Mensaje de WM_THEMECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809548"
---
# <a name="wm_themechanged-message"></a>Mensaje de THEMECHANGED de WM \_

Difundir a cada ventana después de un evento de cambio de tema. Algunos ejemplos de eventos de cambio de tema son la activación de un tema, la desactivación de un tema o una transición de un tema a otro.


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

## <a name="remarks"></a>Observaciones

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Este mensaje lo envía el sistema operativo. Normalmente, las aplicaciones no envían este mensaje.

 

Los temas son especificaciones para la apariencia de los controles, de modo que el elemento visual de un control se trata por separado de su funcionalidad.

Para liberar un identificador de tema existente, llame a [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata). Para adquirir un nuevo identificador de tema, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

Después de la difusión **\_ THEMECHANGED de WM** , cualquier controlador de tema existente no es válido. Una ventana que tenga en cuenta el tema debe liberar y volver a abrir cualquiera de sus identificadores de tema ya existentes cuando reciba el mensaje de **\_ THEMECHANGED de WM** . Si la función [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) devuelve un **valor null**, la ventana debe pintarse como desactivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
