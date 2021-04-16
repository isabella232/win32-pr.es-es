---
title: Mensaje FINDMSGSTRING (commdlg. h)
description: Un cuadro de diálogo Buscar o reemplazar envía el mensaje registrado FINDMSGSTRING al procedimiento de ventana de la ventana propietaria cuando el usuario hace clic en el botón Buscar siguiente, reemplazar o reemplazar todo, o cierra el cuadro de diálogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Cuadros de diálogo de mensaje de FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535260"
---
# <a name="findmsgstring-message"></a>Mensaje FINDMSGSTRING

Un cuadro de diálogo **Buscar** o **reemplazar** envía el mensaje registrado **FINDMSGSTRING** al procedimiento de ventana de la ventana propietaria cuando el usuario hace clic en el botón **Buscar siguiente**, **reemplazar** o **reemplazar todo** , o cierra el cuadro de diálogo.


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) . Los miembros de esta estructura contienen la entrada más reciente del usuario, incluida la cadena que se va a buscar, la cadena de reemplazo (si existe) y las opciones de búsqueda y reemplazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Debe especificar la constante **FINDMSGSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

Al crear el cuadro de diálogo, use el miembro **hwndOwner** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para identificar la ventana que recibirá mensajes **FINDMSGSTRING** .

El miembro **Flags** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) incluye una de las marcas siguientes para indicar el evento que provocó el mensaje.



| Marca                            | Significado                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ DIALOGTERM** (0x00000040) | El cuadro de diálogo se está cerrando. Una vez que la ventana propietaria procesa este mensaje, el identificador del cuadro de diálogo ya no es válido.                                                                                    |
| **Fr \_ FINDNEXT** (0x00000008)   | El usuario hizo clic en el botón **Buscar siguiente** en un cuadro de diálogo **Buscar** o **reemplazar** . El miembro **lpstrFindWhat** especifica la cadena que se va a buscar.                                                         |
| **Fr \_ REEMPLAZAR** (0x00000010)    | El usuario hizo clic en el botón **reemplazar** en un cuadro de diálogo **reemplazar** . El miembro **lpstrFindWhat** especifica la cadena que se va a reemplazar y el miembro **lpstrReplaceWith** especifica la cadena de reemplazo.     |
| **Fr \_ REPLACEALL** (0x00000020) | El usuario hizo clic en el botón **reemplazar todo** en un cuadro de diálogo **reemplazar** . El miembro **lpstrFindWhat** especifica la cadena que se va a reemplazar y el miembro **lpstrReplaceWith** especifica la cadena de reemplazo. |



 

En el caso de los mensajes **Buscar siguiente** o **reemplazar todo** , el miembro de **marcas** puede incluir una o varias de las marcas siguientes para indicar las opciones de búsqueda.



| Marca                           | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ DOWN** (0x00000001)      | Si se establece, se selecciona el botón **abajo** de los botones de radio dirección que indica que el usuario desea buscar desde la ubicación actual hasta el final del documento. Si no se establece el valor de **fr \_ Down** , se selecciona el botón **subir** para que el usuario desee buscar en el principio del documento.       |
| **Fr \_ MATCHCASE** (0x00000004) | Si se establece, la casilla **Coincidir mayúsculas y minúsculas** está activada, lo que indica que el usuario desea que la búsqueda distinga entre mayúsculas y minúsculas. Si no se establece **fr \_ MATCHCASE** , la casilla está desactivada, por lo que la búsqueda no debe distinguir mayúsculas de minúsculas.                                                                         |
| **Fr \_ WHOLEWORD** (0x00000002) | Si se establece, la casilla **coincidir solo con palabras completas** está activada, lo que indica que el usuario desea buscar únicamente palabras completas que coincidan con la cadena de búsqueda. Si no se establece **fr \_ WHOLEWORD** , la casilla está desactivada, por lo que también debe buscar fragmentos de palabras que coincidan con la cadena de búsqueda. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FINDMSGSTRINGW** (Unicode) y **FINDMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

