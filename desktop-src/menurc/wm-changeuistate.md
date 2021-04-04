---
title: Mensaje de WM_CHANGEUISTATE (Winuser. h)
description: Una aplicación envía el mensaje de CHANGEUISTATE de WM \_ para indicar que se debe cambiar el estado de la interfaz de usuario.
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
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803836"
---
# <a name="wm_changeuistate-message"></a>Mensaje de CHANGEUISTATE de WM \_

Una aplicación envía el mensaje de **\_ CHANGEUISTATE de WM** para indicar que se debe cambiar el estado de la interfaz de usuario.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior especifica la acción que se va a realizar. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                   | Significado                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Ius \_ BORRAR**</dt> <dt>2</dt> </dl>                | Las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior deben estar desactivadas.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Ius \_ INICIALIZAr**</dt> <dt>3</dt> </dl> | Las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior deben cambiarse en función del último evento de entrada. Para obtener más información, vea la sección Comentarios.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Ius \_ ESTABLECER**</dt> <dt>1</dt> </dl>                      | Se deben establecer las marcas de estado de la interfaz de usuario especificadas por la palabra de orden superior.<br/>                                                                      |



 

La palabra de orden superior especifica qué elementos de estado de la interfaz de usuario se ven afectados o el estilo del control. Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_**</dt> <dt>0x4</dt> activo </dl>          | Un control debe dibujarse en el estilo utilizado para los controles activos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt> </dl> | Los aceleradores de teclado están ocultos.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Los indicadores de foco están ocultos.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser 0.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una ventana debe enviar este mensaje a sí mismo o a su elemento primario cuando debe cambiar los elementos de estado de la interfaz de usuario de todas las ventanas de la misma jerarquía. El procedimiento de ventana debe permitir que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procese este mensaje para que todo el árbol de la ventana tenga un estado de interfaz de usuario coherente. Cuando la ventana de nivel superior recibe el mensaje de **\_ CHANGEUISTATE de WM** , envía un mensaje de [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con los mismos parámetros a todas las ventanas secundarias. Cuando el sistema procesa el mensaje de **\_ UPDATEUISTATE de WM** , realiza el cambio en el estado de la interfaz de usuario.

Si la palabra de orden inferior de *wParam* es \_ Initialize Initialize, el sistema enviará el mensaje de [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con un estado de IU basado en el último evento de entrada. Por ejemplo, si la última entrada procedía del mouse, el sistema ocultará las señales de teclado. Y, si la última entrada procede del teclado, el sistema mostrará las señales de teclado. Si el estado resultante del procesamiento de **WM \_ CHANGEUISTATE** es el mismo que el anterior, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no envía este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**QUERYUISTATE de WM \_**](wm-queryuistate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

