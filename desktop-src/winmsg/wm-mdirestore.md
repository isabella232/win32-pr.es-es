---
description: Una aplicación envía el mensaje WM MDIRESTORE a una ventana de cliente de interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI de tamaño maximizado \_ o minimizado.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: WM_MDIRESTORE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bc9a8b4a414a1f987ad51b01f94c50b336adb8a32a298a83a1a3b9de8b0bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110705"
---
# <a name="wm_mdirestore-message"></a>Mensaje \_ DE WM MDIRESTORE

Una aplicación envía el **mensaje WM \_ MDIRESTORE** a una ventana de cliente de interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI de tamaño maximizado o minimizado.


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
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




