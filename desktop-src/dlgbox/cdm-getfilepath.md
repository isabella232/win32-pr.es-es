---
title: CDM_GETFILEPATH mensaje (Commdlg.h)
description: Recupera la ruta de acceso y el nombre de archivo del archivo seleccionado en un cuadro de diálogo Abrir o Guardar como de estilo explorador.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ac18880ef62df1d228c006f0bc33fcf4932cbb976419ee29464e49828d8173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786338"
---
# <a name="cdm_getfilepath-message"></a>Mensaje \_ GETFILEPATH de CDM

\[A partir Windows Vista, **los** cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).  Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Recupera la ruta de acceso y el nombre de archivo del archivo seleccionado en un cuadro de diálogo Abrir **o** Guardar **como** de estilo explorador. El cuadro de diálogo debe haber sido creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en caracteres, del búfer *lParam.* Para la versión ANSI, este es el número de bytes; para la versión Unicode, este es el número de caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe el nombre de archivo y la ruta de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en caracteres, del nombre de archivo y la cadena de ruta de acceso, incluido el carácter NULL final. Este es el número de bytes o caracteres copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.

Si se produce un error, el valor devuelto es menor que cero.

## <a name="remarks"></a>Comentarios

La macro correspondiente es la siguiente:

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

