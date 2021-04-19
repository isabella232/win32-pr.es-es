---
title: CDN_INCLUDEITEM de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como para determinar si el cuadro de diálogo debe mostrar un elemento en la lista de elementos de una carpeta de shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM de diálogo del código de notificación
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a91c61e4a7c2786e67ed28e2c62e5963762659c
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590782"
---
# <a name="cdn_includeitem-notification-code"></a>Código de notificación INCLUDEITEM de CDN \_

\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](/windows/win32/shell/common-file-dialog). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Enviado por **un cuadro de** diálogo Abrir o Guardar como para determinar si el cuadro de diálogo debe mostrar un elemento en la lista de elementos de una carpeta de shell.  Cuando el usuario abre una carpeta, el cuadro de diálogo envía una notificación **\_ INCLUDEITEM** de CDN para cada elemento de la carpeta. El cuadro de diálogo envía esta notificación solo si se estableció la marca **OFN \_ ENABLEINCLUDENOTIFY** cuando se creó el cuadro de diálogo.

El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OFNOTIFYEX.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)

La [**estructura OFNOTIFYEX contiene**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ INCLUDEITEM de CDN.**

El **miembro psf** de la [**estructura OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) es un puntero a una interfaz para la carpeta cuyos elementos se enumeran. El **miembro pidl** es un puntero a una lista de identificadores de elemento que identifica el elemento relativo a la carpeta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) devuelve cero, el cuadro de diálogo excluye el elemento de la lista de elementos.

Para incluir el elemento, devuelva un valor distinto de cero del procedimiento de enlace.

## <a name="remarks"></a>Observaciones

El cuadro de diálogo siempre incluye elementos que tienen los atributos **SFGAO \_ FILESYSTEM** y **SFGAO \_ FILESYSANCESTOR,** independientemente del valor devuelto por **\_ CDN INCLUDEITEM**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

