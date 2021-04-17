---
description: Se envía a una aplicación cuando el sistema operativo está a punto de cambiar el IME actual. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Mensaje de WM_IME_SELECT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686817"
---
# <a name="wm_ime_select-message"></a>Mensaje de selección de \_ IME de WM \_

Se envía a una aplicación cuando el sistema operativo está a punto de cambiar el IME actual. Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Indicador de selección. Este parámetro especifica **true** si el IME indicado está seleccionado. El parámetro se establece en **false** si el IME especificado ya no está seleccionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de configuración regional de entrada asociado al IME.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación que ha creado una ventana de IME debe pasar este mensaje a esa ventana para que pueda recuperar el controlador de distribución del teclado al IME recién seleccionado.

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasando la información a la ventana IME predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del administrador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
