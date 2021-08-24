---
description: El mensaje WM CTLCOLOR se usa en versiones de 16 bits de Windows para cambiar la combinación de colores de los cuadros de lista, los cuadros de lista de cuadros combinados, cuadros de mensaje, controles de botón, controles de edición, controles estáticos y cuadros de \_ diálogo. Nota Para obtener información relacionada con este mensaje y las versiones de 32 bits de Windows, vea Comentarios.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: WM_CTLCOLOR mensaje (WindowsX.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c53f18bc42737e44a2137e0c9763dfc41de44f65661ca4754915f7a21317641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343295"
---
# <a name="wm_ctlcolor-message"></a>Mensaje \_ CTLCOLOR de WM

El mensaje **WM \_ CTLCOLOR** se usa en versiones de 16 bits de Windows para cambiar la combinación de colores de los cuadros de lista, los cuadros de lista de cuadros combinados, cuadros de mensaje, controles de botón, controles de edición, controles estáticos y cuadros de diálogo.

> [!Note]  
> Para obtener información relacionada con este mensaje y las versiones de 32 bits de Windows, vea Comentarios.

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana de destino.

</dd> <dt>

*wParam* 
</dt> <dd>

Identificador de un contexto de presentación (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de una ventana secundaria (control).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, devuelve un identificador a un pincel. El sistema usa el pincel para pintar el fondo del control.

## <a name="remarks"></a>Comentarios

El **mensaje \_ WM CTLCOLOR** de 16 bits Windows se ha reemplazado por notificaciones más específicas. Estos reemplazos incluyen lo siguiente:

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORDLG**](../dlgbox/wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WindowsX.h</dt> </dl> |



 

 
