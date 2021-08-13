---
title: CDM_GETFOLDERIDLIST mensaje (Commdlg.h)
description: Recupera la dirección de la lista de identificadores de elemento correspondiente a la carpeta que un cuadro de diálogo Abrir o Guardar como de estilo explorador tiene abierto actualmente.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f6a753cf53bdd2cde53a0e3df973457b50b8ed326a7d7ee50c05dc24f1d0a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786202"
---
# <a name="cdm_getfolderidlist-message"></a>Mensaje \_ GETFOLDERIDLIST de CDM

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]

Recupera la dirección de la lista de identificadores de  elemento correspondiente a la carpeta que un cuadro de diálogo Abrir o Guardar **como** de estilo explorador tiene abierto actualmente. El cuadro de diálogo se debe haber creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en bytes, del búfer *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe la lista de identificadores de elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en bytes, de la lista de identificadores de elemento. Este es el número de bytes copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.

Si se produce un error, el valor devuelto es menor que cero.

## <a name="remarks"></a>Observaciones

La macro correspondiente es la siguiente:

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
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

