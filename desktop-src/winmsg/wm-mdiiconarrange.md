---
description: Una aplicación envía el mensaje de MDIICONARRANGE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Mensaje de WM_MDIICONARRANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497320"
---
# <a name="wm_mdiiconarrange-message"></a>Mensaje de MDIICONARRANGE de WM \_

Una aplicación envía el mensaje de **\_ MDIICONARRANGE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas.


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
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MDICASCADE de WM \_**](wm-mdicascade.md)
</dt> <dt>

[**MDITILE de WM \_**](wm-mditile.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




