---
title: Código de notificación de CDN_INCLUDEITEM (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como para determinar si el cuadro de diálogo debe mostrar un elemento en la lista de elementos de una carpeta de Shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM cuadros de diálogo código de notificación
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
ms.openlocfilehash: 67cbe830c644657425eb087dd64884da17a9a0c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803284"
---
# <a name="cdn_includeitem-notification-code"></a>\_Código de notificación INCLUDEITEM de CDN

\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]

Enviado por un cuadro de diálogo **abrir** o **Guardar como** para determinar si el cuadro de diálogo debe mostrar un elemento en la lista de elementos de una carpeta de Shell. Cuando el usuario abre una carpeta, el cuadro de diálogo envía una notificación **\_ INCLUDEITEM de CDN** para cada elemento de la carpeta. El cuadro de diálogo envía esta notificación solo si se estableció la marca **OFN \_ ENABLEINCLUDENOTIFY** cuando se creó el cuadro de diálogo.

El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .


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

Puntero a una estructura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .

La estructura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación INCLUDEITEM de la **red CDN \_** .

El miembro **PSF** de la estructura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) es un puntero a una interfaz para la carpeta cuyos elementos se están enumerando. El miembro **PIDL** es un puntero a una lista de identificadores de elemento que identifica el elemento relativo a la carpeta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) devuelve cero, el cuadro de diálogo excluye el elemento de la lista de elementos.

Para incluir el elemento, devuelva un valor distinto de cero del procedimiento de enlace.

## <a name="remarks"></a>Observaciones

En el cuadro de diálogo siempre se incluyen los elementos que tienen los atributos **SFGAO \_ FILESYSTEM** y **SFGAO \_ FILESYSANCESTOR** , independientemente del valor devuelto por **CDN \_ INCLUDEITEM**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

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

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

