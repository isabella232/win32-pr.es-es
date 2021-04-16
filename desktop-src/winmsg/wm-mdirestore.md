---
description: Una aplicación envía el mensaje de MDIRESTORE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI de tamaño maximizado o minimizado.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Mensaje de WM_MDIRESTORE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705529"
---
# <a name="wm_mdirestore-message"></a>Mensaje de MDIRESTORE de WM \_

Una aplicación envía el mensaje de **\_ MDIRESTORE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI de tamaño maximizado o minimizado.


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria MDI que se va a restaurar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **cero**

El valor devuelto siempre es cero.

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

[**MDIMAXIMIZE de WM \_**](wm-mdimaximize.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




