---
description: Una aplicación envía el mensaje de MDICASCADE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias en un formato en cascada.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Mensaje de WM_MDICASCADE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360239"
---
# <a name="wm_mdicascade-message"></a>Mensaje de MDICASCADE de WM \_

Una aplicación envía el mensaje de **\_ MDICASCADE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias en un formato en cascada.


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
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt> </dl> | Impide que las ventanas secundarias MDI deshabilitadas se puedan poner en cascada. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_ ZORDER**</dt> <dt>0x0004</dt> </dl>                   | Organiza las ventanas en orden Z.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Si el mensaje se realiza correctamente, el valor devuelto es **true**.

Si se produce un error en el mensaje, el valor devuelto es **false**.

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

[**MDIICONARRANGE de WM \_**](wm-mdiiconarrange.md)
</dt> <dt>

[**MDITILE de WM \_**](wm-mditile.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




