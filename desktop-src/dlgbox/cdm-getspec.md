---
title: CDM_GETSPEC mensaje (Commdlg.h)
description: Recupera el nombre de archivo (sin incluir la ruta de acceso) del archivo seleccionado actualmente en un cuadro de diálogo Abrir o Guardar como de estilo explorador.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- CDM_GETSPEC cuadros de diálogo del mensaje
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66e919ccbdabbb19745b172082eed5cc2b0b8a36555587cda59bd7e24fca3247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022525"
---
# <a name="cdm_getspec-message"></a>Mensaje \_ GETSPEC de CDM

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]

Recupera el nombre de archivo (sin incluir la ruta de  acceso) del archivo seleccionado actualmente en un cuadro de diálogo Abrir o **Guardar como** de estilo explorador. El cuadro de diálogo se debe haber creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en caracteres, del búfer *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe el nombre de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en caracteres, de la cadena de nombre de archivo, incluido el carácter NULL final. Este es el número de bytes o caracteres copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.

Si se produce un error, el valor devuelto es menor que cero.

## <a name="remarks"></a>Comentarios

La macro correspondiente es la siguiente:

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

