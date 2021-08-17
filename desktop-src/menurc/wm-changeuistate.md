---
title: WM_CHANGEUISTATE mensaje (Winuser.h)
description: Una aplicación envía el mensaje \_ CHANGEUISTATE de WM para indicar que se debe cambiar el estado de la interfaz de usuario.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3849f9a5d2ccd0cec1bcaba4280e125ea01a669c8535c2dc520ebb98c3a3fcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869715"
---
# <a name="wm_changeuistate-message"></a>Mensaje \_ CHANGEUISTATE de WM

Una aplicación envía el mensaje **\_ CHANGEUISTATE** de WM para indicar que se debe cambiar el estado de la interfaz de usuario.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica la acción que se va a realizar. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                   | Significado                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIS \_ CLEAR**</dt> <dt>2</dt> </dl>                | Se deben borrar las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIS \_ INICIALIZAR**</dt> <dt>3</dt> </dl> | Las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior deben cambiarse en función del último evento de entrada. Para obtener más información, vea la sección Comentarios.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIS \_ SET**</dt> <dt>1</dt> </dl>                      | Se deben establecer las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior.<br/>                                                                      |



 

La palabra de orden superior especifica qué elementos de estado de la interfaz de usuario se ven afectados o el estilo del control. Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ Active**</dt> <dt>0x4</dt> </dl>          | Se debe dibujar un control en el estilo utilizado para los controles activos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HideACCEL**</dt> <dt>0x2</dt> </dl> | Los aceleradores de teclado están ocultos.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HideFOCUS**</dt> <dt>0x1</dt> </dl> | Los indicadores de foco están ocultos.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser 0.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una ventana debe enviar este mensaje a sí misma o a su elemento primario cuando debe cambiar los elementos de estado de la interfaz de usuario de todas las ventanas de la misma jerarquía. El procedimiento de ventana debe permitir [**que DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procese este mensaje para que todo el árbol de ventana tenga un estado de interfaz de usuario coherente. Cuando la ventana de nivel superior recibe el mensaje **\_ CHANGEUISTATE** de WM, envía un mensaje [**\_ UPDATEUISTATE**](wm-updateuistate.md) de WM con los mismos parámetros a todas las ventanas secundarias. Cuando el sistema procesa el **mensaje \_ UPDATEUISTATE de WM,** realiza el cambio en el estado de la interfaz de usuario.

Si la palabra de orden bajo de *wParam* es UIS INITIALIZE, el sistema enviará el mensaje \_ [**\_ UPDATEUISTATE**](wm-updateuistate.md) de WM con un estado de interfaz de usuario basado en el último evento de entrada. Por ejemplo, si la última entrada provenía del mouse, el sistema ocultará las indicaciones del teclado. Y, si la última entrada provenía del teclado, el sistema mostrará las indicaciones del teclado. Si el estado que resulta del procesamiento **de WM \_ CHANGEUISTATE** es el mismo que el estado anterior, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no envía este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

