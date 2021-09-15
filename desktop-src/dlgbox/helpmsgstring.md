---
title: Mensaje HELPMSGSTRING (Commdlg.h)
description: Un cuadro de diálogo común envía el mensaje registrado HELPMSGSTRING al procedimiento de ventana de su ventana propietaria cuando el usuario hace clic en el botón Ayuda.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Cuadros de diálogo del mensaje HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359006"
---
# <a name="helpmsgstring-message"></a>Mensaje HELPMSGSTRING

Un cuadro de diálogo común envía el mensaje **registrado HELPMSGSTRING** al procedimiento de ventana de su ventana propietaria cuando el usuario hace clic en el **botón Ayuda.**


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del cuadro de diálogo común.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura de inicialización del cuadro de diálogo común. Esta estructura puede ser una [**estructura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) [**o PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Debe especificar la **constante HELPMSGSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

Al crear el cuadro de diálogo, use el **miembro hwndOwner** de la estructura de inicialización para identificar la ventana para recibir **mensajes HELPMSGSTRING.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HELPMSGSTRINGW** (Unicode) y **HELPMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_CDN AYUDA**](cdn-help.md)
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

