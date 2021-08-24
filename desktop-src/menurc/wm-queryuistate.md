---
title: WM_QUERYUISTATE mensaje (Winuser.h)
description: Una aplicación envía el mensaje \_ QUERYUISTATE de WM para recuperar el estado de la interfaz de usuario de una ventana.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e62fc33fb79594f3e07c0d44d4b25fd16e980ef3a4a89b3079c69ef6eb5d1b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119267915"
---
# <a name="wm_queryuistate-message"></a>Mensaje \_ DE WM QUERYUISTATE

Una aplicación envía el mensaje **\_ QUERYUISTATE de WM** para recuperar el estado de la interfaz de usuario de una ventana.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **NULL si** los indicadores de foco y los aceleradores de teclado están visibles. De lo contrario, el valor devuelto puede ser uno o varios de los valores siguientes.



| Código o valor devuelto                                                                                                                                       | Descripción                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_ Active**</dt> <dt>0x4</dt> </dl>    | Se debe dibujar un control en el estilo utilizado para los controles activos.<br/> |
| <dl> <dt>**UISF \_ HideACCEL**</dt> <dt>0x2</dt> </dl> | Los aceleradores de teclado están ocultos.<br/>                                |
| <dl> <dt>**UISF \_ HideFOCUS**</dt> <dt>0x1</dt> </dl> | Los indicadores de foco están ocultos.<br/>                                     |



 

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

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ UPDATEUISTATE**](wm-updateuistate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

 





