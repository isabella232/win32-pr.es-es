---
description: Se envía a la ventana primaria de un control o menú dibujado por el propietario cuando ha cambiado un aspecto visual del control o menú.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Mensaje de DFM_WM_DRAWITEM (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984294"
---
# <a name="dfm_wm_drawitem-message"></a>Mensaje de DFM \_ WM \_ DRAWITEM

Se envía a la ventana primaria de un control o menú dibujado por el propietario cuando ha cambiado un aspecto visual del control o menú.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Identificador del control que envió el mensaje de **DFM \_ WM \_ DRAWITEM** . Si el mensaje se envió mediante un menú, este parámetro es cero.

</dd> <dt>

*lpDrawItem* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información sobre el elemento que se va a dibujar y el tipo de dibujo necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **true**.

## <a name="remarks"></a>Observaciones

El miembro **del itemaction** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica la operación de dibujo que una aplicación debe realizar.

Antes de volver a procesar este mensaje, una aplicación debe asegurarse de que el contexto de dispositivo identificado por el miembro **HDC** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) está en el estado predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
