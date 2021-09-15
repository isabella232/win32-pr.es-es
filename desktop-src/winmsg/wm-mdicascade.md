---
description: Una aplicación envía el mensaje WM MDICASCADE a una ventana cliente de interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias \_ en un formato en cascada.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: WM_MDICASCADE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466506"
---
# <a name="wm_mdicascade-message"></a>Mensaje \_ MDICASCADE de WM

Una aplicación envía el **mensaje \_ WM MDICASCADE** a una ventana cliente de interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias en un formato en cascada.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Comportamiento en cascada. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                          | Significado                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt> </dl> | Impide que las ventanas secundarias MDI deshabilitadas se conecten en cascada. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_ ZORDER**</dt> <dt>0x0004</dt> </dl>                   | Organiza las ventanas en orden Z.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Si el mensaje se realiza correctamente, el valor devuelto es **TRUE.**

Si se produce un error en el mensaje, el valor devuelto es **FALSE.**

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

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

[**WM \_ MDITILE**](wm-mditile.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




