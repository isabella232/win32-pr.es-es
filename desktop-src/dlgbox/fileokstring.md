---
title: Mensaje FILEOKSTRING (Commdlg.h)
description: Un cuadro de diálogo Abrir o Guardar como envía el mensaje registrado FILEOKSTRING al procedimiento de enlace, OFNHookProc, cuando el usuario especifica un nombre de archivo y hace clic en el botón Aceptar.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Cuadros de diálogo del mensaje FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241359"
---
# <a name="fileokstring-message"></a>Mensaje FILEOKSTRING

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Un **cuadro** de **diálogo** Abrir o Guardar como envía el mensaje **registrado FILEOKSTRING** al procedimiento de enlace, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), cuando el usuario especifica un nombre de archivo y hace clic en el **botón** Aceptar. El procedimiento de enlace puede aceptar el nombre de archivo y permitir que el cuadro de diálogo se cierre, o rechazar el nombre de archivo y forzar que el cuadro de diálogo permanezca abierto.


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) El **miembro lpstrFile** de esta estructura contiene la unidad, la ruta de acceso y el nombre de archivo especificados por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace  devuelve cero, **el** cuadro de diálogo Abrir o Guardar como acepta el nombre de archivo especificado y se cierra.

Si el procedimiento de enlace devuelve  un  valor distinto de cero, el cuadro de diálogo Abrir o Guardar como rechaza el nombre de archivo especificado y permanece abierto.

## <a name="remarks"></a>Observaciones

El procedimiento de enlace debe especificar la **constante FILEOKSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FILEOKSTRINGW** (Unicode) y **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_CDN FILEOK**](cdn-fileok.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

