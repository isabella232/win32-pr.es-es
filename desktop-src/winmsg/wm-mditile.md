---
description: Una aplicación envía el mensaje de MDITILE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI en formato de mosaico.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Mensaje de WM_MDITILE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275350"
---
# <a name="wm_mditile-message"></a>Mensaje de MDITILE de WM \_

Una aplicación envía el mensaje de **\_ MDITILE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para organizar todas las ventanas secundarias MDI en formato de mosaico.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La opción de mosaico. Este parámetro puede ser uno de los siguientes valores, combinados opcionalmente con **MDITILE \_ SKIPDISABLED** para evitar que las ventanas secundarias MDI deshabilitadas se coloquen en mosaico.



| Value                                                                                                                                                                                                                                    | Significado                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0001</dt> horizontal </dl> | Mosaicos ventanas horizontalmente.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0000</dt> vertical </dl>       | Mosaicos ventanas verticalmente.<br/>   |



 

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

[**MDICASCADE de WM \_**](wm-mdicascade.md)
</dt> <dt>

[**MDIICONARRANGE de WM \_**](wm-mdiiconarrange.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




