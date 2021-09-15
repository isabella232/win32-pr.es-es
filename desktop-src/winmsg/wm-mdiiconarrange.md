---
description: Una aplicación envía el mensaje WM MDIICONARRANGE a una ventana de cliente de interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias \_ MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: WM_MDIICONARRANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571297"
---
# <a name="wm_mdiiconarrange-message"></a>Mensaje \_ MDIICONARRANGE de WM

Una aplicación envía el **mensaje \_ WM MDIICONARRANGE** a una ventana de cliente de interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas.


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

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

[**WM \_ MDICASCADE**](wm-mdicascade.md)
</dt> <dt>

[**WM \_ MDITILE**](wm-mditile.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




