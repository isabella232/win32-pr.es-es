---
description: Una aplicación envía el mensaje WM MDIRESTORE a una ventana cliente de interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI a partir de un tamaño maximizado \_ o minimizado.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: WM_MDIRESTORE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466728"
---
# <a name="wm_mdirestore-message"></a>Mensaje \_ DE WM MDIRESTORE

Una aplicación envía el **mensaje WM \_ MDIRESTORE** a una ventana cliente de interfaz de múltiples documentos (MDI) para restaurar una ventana secundaria MDI a partir de un tamaño maximizado o minimizado.


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria de MDI que se va a restaurar.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




