---
title: PROPSHEETCFG (estructura)
description: Se usa para contener datos de configuración de hoja de propiedades.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Propiedades de la estructura PROPSHEETCFG Active Directory
- Puntero de estructura PPROPSHEETCFG Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 971296e1e269e977919f142d1efe24426b9c83f19ac26da2e2362ab48da0aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025443"
---
# <a name="propsheetcfg-structure"></a>PROPSHEETCFG (estructura)

La **estructura PROPSHEETCFG** se usa para contener datos de configuración de hoja de propiedades. Esta estructura se encuentra en el formato del Portapapeles [**\_ \_ PROPSHEETCONFIG de CFSTR DS.**](cfstr-ds-propsheetconfig.md)

> [!Note]  
> Esta estructura no se define en un archivo de encabezado publicado. Para usar esta estructura, debe definirla usted mismo en el formato exacto que se muestra.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>Miembros

<dl> <dt>

**lNotifyHandle**
</dt> <dd>

Contiene el identificador de notificación. Esto es idéntico al identificador pasado para el parámetro *handle* [**en el método IExtendPropertySheet2::CreatePropertyPages.**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85))

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

Contiene el identificador de ventana de la hoja de propiedades primaria.

</dd> <dt>

**hwndHidden**
</dt> <dd>

Contiene el identificador de la ventana oculta.

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

Contiene un valor de 32 bits definido por la aplicación. Este valor se pasa a la aplicación en *el wParam* del mensaje [**WM \_ DSA \_ SHEET CLOSE \_ \_ NOTIFY.**](wm-dsa-sheet-close-notify.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**NOTIFICACIÓN \_ DE CIERRE DE HOJA DE WM DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

