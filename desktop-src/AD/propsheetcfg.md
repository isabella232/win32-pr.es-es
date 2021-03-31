---
title: Estructura PROPSHEETCFG
description: Se usa para contener los datos de configuración de la hoja de propiedades.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory de la estructura PROPSHEETCFG
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
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079408"
---
# <a name="propsheetcfg-structure"></a>Estructura PROPSHEETCFG

La estructura **PROPSHEETCFG** se usa para contener los datos de configuración de la hoja de propiedades. Esta estructura se incluye en el formato del portapapeles [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) .

> [!Note]  
> Esta estructura no está definida en un archivo de encabezado publicado. Para usar esta estructura, debe definirla usted mismo en el formato exacto que se muestra.

 

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

Contiene el identificador de notificación. Es idéntico al identificador pasado para el parámetro *Handle* en el método [**IExtendPropertySheet2:: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .

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

Contiene un valor de 32 bits definido por la aplicación. Este valor se devuelve a la aplicación en el *wParam* del mensaje de [**notificación de cierre de la \_ \_ hoja \_ \_ DSA de WM**](wm-dsa-sheet-close-notify.md) .

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

[**\_notificación de \_ cierre de hoja DSA \_ de WM \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

