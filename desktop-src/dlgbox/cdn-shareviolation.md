---
title: CDN_SHAREVIOLATION de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el usuario hace clic en el botón Aceptar y se produce una infracción de uso compartido de red para el archivo seleccionado.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION cuadro de diálogo de código de notificación
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590702"
---
# <a name="cdn_shareviolation-notification-code"></a>Código de notificación \_ DE SHAREVIOLATION de CDN

\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](/windows/win32/shell/common-file-dialog). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Enviado por un  cuadro de diálogo Abrir o Guardar  **como** de estilo explorador cuando el usuario hace clic en el botón Aceptar y se produce una infracción de uso compartido de red para el archivo seleccionado.

El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) El **miembro pszFile** de esta estructura es un puntero al nombre del archivo que tenía la infracción de uso compartido. La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de notificación **\_ SHAREVIOLATION de CDN.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto indica cómo el cuadro de diálogo debe controlar la infracción de uso compartido.

Si el procedimiento de enlace devuelve cero, el cuadro de diálogo muestra el mensaje de advertencia estándar para una infracción de uso compartido.

Para evitar la presentación del mensaje de advertencia estándar, devuelva un valor distinto de cero del procedimiento de enlace y llame a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer uno de los siguientes valores **\_ msgRESULT de DWL.**



| Código o valor devuelto                                                                                                                                           | Descripción                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Hace que el cuadro de diálogo devuelva el nombre de archivo sin advertir al usuario sobre la infracción de uso compartido.<br/>  |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Hace que el cuadro de diálogo rechace el nombre de archivo sin advertir al usuario sobre la infracción de uso compartido. <br/> |



 

## <a name="remarks"></a>Observaciones

El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**

El sistema envía esta notificación solo si no se especificó el valor **OFN \_ SHAREAWARE** cuando se creó el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluye Windows.h)</dt> </dl> |



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

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

