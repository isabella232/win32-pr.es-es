---
title: WM_UPDATEUISTATE mensaje (Winuser.h)
description: Una aplicación envía el mensaje UPDATEUISTATE de WM para cambiar el estado de la interfaz de usuario de \_ la ventana especificada y de todas sus ventanas secundarias.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351770019f18c52c4ff1588a09c803d07f0f58ce032b35af53501ff4e47b6aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112865"
---
# <a name="wm_updateuistate-message"></a>Mensaje \_ UPDATEUISTATE de WM

Una aplicación envía el mensaje **\_ UPDATEUISTATE** de WM para cambiar el estado de la interfaz de usuario de la ventana especificada y de todas sus ventanas secundarias.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica la acción que se va a realizar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIS \_ CLEAR**</dt> <dt>2</dt> </dl>                | El elemento de estado de la interfaz de usuario especificado por la palabra de orden superior debe estar oculto.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIS \_ INICIALIZAR**</dt> <dt>3</dt> </dl> | El elemento de estado de la interfaz de usuario especificado por la palabra de orden superior debe cambiarse en función del último evento de entrada. Para obtener más información, vea la sección Comentarios.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIS \_ SET**</dt> <dt>1</dt> </dl>                      | El elemento de estado de la interfaz de usuario especificado por la palabra de orden superior debe estar visible.<br/>                                                                  |



 

La palabra de orden superior especifica qué elementos de estado de la interfaz de usuario se ven afectados o el estilo del control. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ Active**</dt> <dt>0x4</dt> </dl>          | Se debe dibujar un control en el estilo utilizado para los controles activos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HideACCEL**</dt> <dt>0x2</dt> </dl> | Aceleradores de teclado.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HideFOCUS**</dt> <dt>0x1</dt> </dl> | Indicadores de foco.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una ventana debe enviar este mensaje para cambiar el estado de la interfaz de usuario de todas sus ventanas secundarias. A diferencia del mensaje [**\_ CHANGEUISTATE**](wm-changeuistate.md) de WM, que es una notificación, cuando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa el mensaje **\_ UPDATEUISTATE** de WM, cambia el estado de la interfaz de usuario y propaga los cambios a todas las ventanas secundarias.

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) actualiza el estado de la interfaz de usuario según el *valor wParam.* Si se modifica el estado de la interfaz de usuario, la función envía el mensaje a todas las ventanas secundarias inmediatas. **DefWindowProc también** envía este mensaje cuando recibe un mensaje [**\_ CHANGEUISTATE**](wm-changeuistate.md) de WM que notifica al sistema que una ventana secundaria pretende modificar el estado de la interfaz de usuario.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

