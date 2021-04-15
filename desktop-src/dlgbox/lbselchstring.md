---
title: Mensaje LBSELCHSTRING (commdlg. h)
description: Un cuadro de diálogo abrir o guardar como envía el mensaje registrado LBSELCHSTRING al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Cuadros de diálogo de mensaje de LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14538c429bf943e4557974166bd7da747176bd93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695977"
---
# <a name="lbselchstring-message"></a>Mensaje LBSELCHSTRING

\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]

Un cuadro de diálogo **abrir** o **Guardar como** envía el mensaje registrado **LBSELCHSTRING** al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del cuadro de lista o cuadro combinado en el que ha cambiado la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica el número de elemento de la cadena seleccionada en el cuadro de lista o el cuadro combinado. La palabra de orden superior especifica el tipo de cambio de selección. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                       | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ de LBSELCHANGE**</dt> <dt>0</dt> </dl>     | El elemento es el único elemento seleccionado en un cuadro de lista de selección única.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ de LBSELADD**</dt> <dt>2</dt> </dl>              | El elemento es uno de los elementos seleccionados en un cuadro de lista de selección múltiple.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ de LBSELSUB**</dt> <dt>1</dt> </dl>              | El elemento ya no está seleccionado en un cuadro de lista de selección múltiple.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ de LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | No existe ningún elemento en un cuadro de lista de selección múltiple.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

El procedimiento de enlace debe especificar la constante **LBSELCHSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LBSELCHSTRINGW** (Unicode) y **LBSELCHSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SELCHANGE de CDN \_**](cdn-selchange.md)
</dt> <dt>

[**TYPECHANGE de CDN \_**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

