---
description: Una aplicación envía el mensaje de MDIMAXIMIZE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para maximizar una ventana secundaria MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Mensaje de WM_MDIMAXIMIZE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715063"
---
# <a name="wm_mdimaximize-message"></a>Mensaje de MDIMAXIMIZE de WM \_

Una aplicación envía el mensaje de **\_ MDIMAXIMIZE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para maximizar una ventana secundaria MDI. El sistema cambia el tamaño de la ventana secundaria para que su área cliente rellene la ventana del cliente. El sistema coloca el icono de menú ventana de la ventana secundaria en la posición más a la derecha de la barra de menús de la ventana de marco y coloca el icono de restauración de la ventana secundaria en la posición más a la izquierda. El sistema también anexa el texto de la barra de título de la ventana secundaria al de la ventana de marco.


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria MDI que se va a maximizar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **cero**

El valor devuelto siempre es cero.

## <a name="remarks"></a>Observaciones

Si una ventana de cliente MDI recibe cualquier mensaje que cambie la activación de sus ventanas secundarias mientras se maximiza la ventana secundaria MDI activa actualmente, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.

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

[**MDIRESTORE de WM \_**](wm-mdirestore.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




