---
description: El mensaje de CTLCOLOR de WM \_ se usa en las versiones de 16 bits de Windows para cambiar la combinación de colores de los cuadros de lista, los cuadros de lista de los cuadros combinados, los cuadros de mensaje, los controles de botón, los controles de edición, los controles estáticos y los cuadros de diálogo. Nota para obtener información relacionada con este mensaje y con las versiones de 32 bits de Windows, consulte la sección Comentarios.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Mensaje de WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660717"
---
# <a name="wm_ctlcolor-message"></a>Mensaje de CTLCOLOR de WM \_

El mensaje de **\_ CTLCOLOR de WM** se usa en las versiones de 16 bits de Windows para cambiar la combinación de colores de los cuadros de lista, los cuadros de lista de los cuadros combinados, los cuadros de mensaje, los controles de botón, los controles de edición, los controles estáticos y los cuadros de diálogo.

> [!Note]  
> Para obtener información relacionada con este mensaje y versiones de 32 bits de Windows, consulte la sección Comentarios.

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
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

Si una aplicación procesa este mensaje, devuelve un identificador a un pincel. El sistema utiliza el pincel para pintar el fondo del control.

## <a name="remarks"></a>Observaciones

El mensaje de **\_ CTLCOLOR de WM** de Windows de 16 bits se ha sustituido por notificaciones más específicas. Entre estos reemplazos se incluyen los siguientes:

-   [**CTLCOLORBTN de WM \_**](../controls/wm-ctlcolorbtn.md)
-   [**CTLCOLOREDIT de WM \_**](../controls/wm-ctlcoloredit.md)
-   [**CTLCOLORDLG de WM \_**](../dlgbox/wm-ctlcolordlg.md)
-   [**CTLCOLORLISTBOX de WM \_**](../controls/wm-ctlcolorlistbox.md)
-   [**CTLCOLORSCROLLBAR de WM \_**](../controls/wm-ctlcolorscrollbar.md)
-   [**CTLCOLORSTATIC de WM \_**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WindowsX. h</dt> </dl> |



 

 
