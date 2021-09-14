---
title: Mensaje LBSELCHSTRING (Commdlg.h)
description: Un cuadro de diálogo Abrir o Guardar como envía el mensaje registrado LBSELCHSTRING al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Cuadros de diálogo del mensaje LBSELCHSTRING
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
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966404"
---
# <a name="lbselchstring-message"></a>Mensaje LBSELCHSTRING

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]

Un **cuadro de** diálogo Abrir o Guardar como envía el mensaje registrado  **LBSELCHSTRING** al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del cuadro de lista o cuadro combinado en el que cambió la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica el número de elemento de la cadena seleccionada en el cuadro de lista o cuadro combinado. La palabra de orden superior especifica el tipo de cambio de selección. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                       | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt> </dl>     | El elemento es el único elemento seleccionado en un cuadro de lista de selección única.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ LBSELADD**</dt> <dt>2</dt> </dl>              | El elemento es uno de los elementos seleccionados en un cuadro de lista de selección múltiple.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ LBSELSUB**</dt> <dt>1</dt> </dl>              | El elemento ya no está seleccionado en un cuadro de lista de selección múltiple.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | No existe ningún elemento en un cuadro de lista de selección múltiple.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

El procedimiento de enlace debe especificar la **constante LBSELCHSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LBSELCHSTRINGW** (Unicode) y **LBSELCHSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_CDN SELCHANGE**](cdn-selchange.md)
</dt> <dt>

[**\_CDN TYPECHANGE**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

