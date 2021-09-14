---
title: Mensaje FINDMSGSTRING (Commdlg.h)
description: Un cuadro de diálogo Buscar o reemplazar envía el mensaje registrado FINDMSGSTRING al procedimiento de ventana de su ventana propietaria cuando el usuario hace clic en el botón Buscar siguiente, Reemplazar o Reemplazar todo, o cierra el cuadro de diálogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Cuadros de diálogo del mensaje FINDMSGSTRING
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241353"
---
# <a name="findmsgstring-message"></a>Mensaje FINDMSGSTRING

Un  cuadro  de diálogo Buscar o reemplazar envía el mensaje registrado **FINDMSGSTRING** al procedimiento de ventana  de su ventana propietaria cuando el usuario hace clic en el botón Buscar **siguiente,** Reemplazar o Reemplazar todo, o cierra el cuadro de diálogo.


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

Puntero a una [**estructura FINDREPLACE.**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) Los miembros de esta estructura contienen la entrada de usuario más reciente, incluida la cadena que se va a buscar, la cadena de reemplazo (si la hay) y las opciones de búsqueda y reemplazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Debe especificar la **constante FINDMSGSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

Al crear el cuadro de diálogo, use el **miembro hwndOwner** de la estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para identificar la ventana para recibir **mensajes FINDMSGSTRING.**

El **miembro Flags** de la [**estructura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) incluye una de las marcas siguientes para indicar el evento que produjo el mensaje.



| Marca                            | Significado                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** (0x00000040) | El cuadro de diálogo se está cerrando. Una vez que la ventana de propietario procesa este mensaje, un identificador para el cuadro de diálogo ya no es válido.                                                                                    |
| **FR \_ FINDNEXT** (0x00000008)   | El usuario hizo clic en **el botón Buscar** siguiente en un cuadro **de** **diálogo** Buscar o reemplazar. El **miembro lpstrFindWhat** especifica la cadena que se va a buscar.                                                         |
| **FR \_ REPLACE** (0x00000010)    | El usuario hizo clic en **el botón Reemplazar** en un cuadro **de** diálogo Reemplazar. El **miembro lpstrFindWhat** especifica la cadena que se va a reemplazar y el **miembro lpstrReplaceWith** especifica la cadena de reemplazo.     |
| **FR \_ REPLACEALL** (0x00000020) | El usuario hizo clic en **el botón Reemplazar** todo en un cuadro **de** diálogo Reemplazar. El **miembro lpstrFindWhat** especifica la cadena que se va a reemplazar y el **miembro lpstrReplaceWith** especifica la cadena de reemplazo. |



 

Para un **mensaje Buscar siguiente** o Reemplazar todo, el miembro **Flags** puede incluir una o varias de las marcas siguientes para indicar las opciones de búsqueda. 



| Marca                           | Significado                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DOWN** (0x00000001)      | Si se establece, se **selecciona el** botón Down (Bajar) de los botones de radio direction (Dirección) que indica que el usuario desea buscar desde la ubicación actual hasta el final del documento. Si **FR \_ DOWN** no está establecido, se **selecciona** el botón Arriba para que el usuario quiera buscar al principio del documento.       |
| **FR \_ MATCHCASE** (0x00000004) | Si se establece, la **casilla Caso** de coincidencia está activada, lo que indica que el usuario quiere que la búsqueda distingue mayúsculas de minúsculas. Si **FR \_ MATCHCASE** no está establecido, la casilla no está seleccionada, por lo que la búsqueda no debe tener en cuenta las mayúsculas y minúsculas.                                                                         |
| **FR \_ WHOLEWORD** (0x00000002) | Si se establece, la **casilla** Coincidir solo palabras enteras está activada, lo que indica que el usuario desea buscar solo palabras enteras que coincidan con la cadena de búsqueda. Si **FR \_ WHOLEWORD** no está establecido, la casilla no está seleccionada, por lo que también debe buscar fragmentos de palabras que coincidan con la cadena de búsqueda. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FINDMSGSTRINGW** (Unicode) y **FINDMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

