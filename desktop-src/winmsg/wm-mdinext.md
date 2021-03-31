---
description: Una aplicación envía el mensaje de MDINEXT de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para activar la ventana secundaria siguiente o anterior.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Mensaje de WM_MDINEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809554"
---
# <a name="wm_mdinext-message"></a>Mensaje de MDINEXT de WM \_

Una aplicación envía el mensaje de **\_ MDINEXT de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para activar la ventana secundaria siguiente o anterior.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria MDI. El sistema activa la ventana secundaria que está inmediatamente antes o después de la ventana secundaria especificada, en función del valor del parámetro *lParam* . Si el parámetro *wParam* es **null**, el sistema activa la ventana secundaria que está inmediatamente antes o después de la ventana secundaria activa actualmente.

</dd> <dt>

*lParam* 
</dt> <dd>

Si este parámetro es cero, el sistema activa la ventana secundaria MDI siguiente y coloca la ventana secundaria identificada por el parámetro *wParam* detrás de las demás ventanas secundarias. Si este parámetro es distinto de cero, el sistema activa la ventana secundaria anterior, colocándolo delante de la ventana secundaria identificada por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **cero**

El valor devuelto siempre es cero.

## <a name="remarks"></a>Observaciones

Si una ventana de cliente MDI recibe cualquier mensaje que cambie la activación de sus ventanas secundarias mientras la ventana secundaria MDI activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.

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

[**MDIACTIVATE de WM \_**](wm-mdiactivate.md)
</dt> <dt>

[**MDIGETACTIVE de WM \_**](wm-mdigetactive.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




