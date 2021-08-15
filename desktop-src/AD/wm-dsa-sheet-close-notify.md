---
title: WM_DSA_SHEET_CLOSE_NOTIFY mensaje
description: Se publica en Active Directory complemento MMC cuando se destruye una hoja de propiedades secundaria.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181679"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>Mensaje DE NOTIFICACIÓN DE CIERRE DE HOJA DE WM \_ DSA \_ \_ \_

El **mensaje WM \_ DSA \_ SHEET CLOSE \_ \_ NOTIFY** se publica en Active Directory complemento MMC cuando se destruye una hoja de propiedades secundaria.

> [!Note]  
> Este valor de mensaje no se define en un archivo de encabezado publicado. Para usar este valor de mensaje, debe definirlo usted mismo en el formato exacto que se muestra.

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de ventana de la ventana de complemento que procesará este mensaje. Este identificador se obtiene del **miembro hwndHidden** de la [**estructura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un valor de 32 bits definido por la aplicación. Esto se obtiene del miembro **wParamSheetClose** de la [**estructura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 





