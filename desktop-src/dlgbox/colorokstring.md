---
title: Mensaje COLOROKSTRING (Commdlg.h)
description: Un cuadro de diálogo Color envía el mensaje registrado COLOROKSTRING al procedimiento de enlace, CCHookProc, cuando el usuario selecciona un color y hace clic en el botón Aceptar.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Cuadros de diálogo del mensaje COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd55db4bb935880438290a83cd99c420ebcabf23ca8cb1bb238ea15f39e06247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726285"
---
# <a name="colorokstring-message"></a>Mensaje COLOROKSTRING

Un **cuadro de** diálogo Color envía el mensaje registrado **COLOROKSTRING** al procedimiento de enlace, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), cuando el usuario selecciona un color y hace clic en el **botón** Aceptar. El procedimiento de enlace puede aceptar el color y permitir que el cuadro de diálogo se cierre o rechazar el color y forzar que el cuadro de diálogo permanezca abierto.


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) El **miembro rgbResult** de esta estructura contiene el valor de color RGB del color seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve cero, el cuadro de diálogo **Color** acepta el color seleccionado y se cierra.

Si el procedimiento de enlace devuelve un valor distinto de cero, el cuadro de diálogo **Color** rechaza el color seleccionado y permanece abierto.

## <a name="remarks"></a>Comentarios

El procedimiento de enlace debe especificar la **constante COLOROKSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **COLOROKSTRINGW** (Unicode) y **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

