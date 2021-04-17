---
title: Mensaje de WM_QUERYUISTATE (Winuser. h)
description: Una aplicación envía el mensaje de QUERYUISTATE de WM \_ para recuperar el estado de la interfaz de usuario de una ventana.
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
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696058"
---
# <a name="wm_queryuistate-message"></a>Mensaje de QUERYUISTATE de WM \_

Una aplicación envía el mensaje de **\_ QUERYUISTATE de WM** para recuperar el estado de la interfaz de usuario de una ventana.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **null** si están visibles los indicadores de foco y los aceleradores de teclado. De lo contrario, el valor devuelto puede ser uno o varios de los valores siguientes.



| Código o valor devuelto                                                                                                                                       | Descripción                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_**</dt> <dt>0x4</dt> activo </dl>    | Un control debe dibujarse en el estilo utilizado para los controles activos.<br/> |
| <dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt> </dl> | Los aceleradores de teclado están ocultos.<br/>                                |
| <dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Los indicadores de foco están ocultos.<br/>                                     |



 

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

[**CHANGEUISTATE de WM \_**](wm-changeuistate.md)
</dt> <dt>

[**UPDATEUISTATE de WM \_**](wm-updateuistate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

 





