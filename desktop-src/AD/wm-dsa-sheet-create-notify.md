---
title: WM_DSA_SHEET_CREATE_NOTIFY mensaje
description: Se publica en Active Directory complemento MMC para crear una hoja de propiedades secundaria.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51fc850504eb4455a41b881aed1109554d0482a8f889fafa2eaf7050488e450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024193"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>Mensaje CREATE NOTIFY de WM \_ DSA \_ SHEET \_ \_

El mensaje CREATE NOTIFY de **WM \_ DSA \_ SHEET \_ \_** se publica en Active Directory complemento MMC para crear una hoja de propiedades secundaria.

> [!Note]  
> Este valor de mensaje no está definido en un archivo de encabezado publicado. Para usar este valor de mensaje, defónozcalo en el formato exacto que se muestra.

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de ventana de la ventana de complemento que procesará este mensaje. Este identificador se obtiene del miembro **hwndHidden** de la [**estructura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntero a una estructura [**DSA \_ SEC \_ PAGE \_ INFO**](dsa-sec-page-info.md) que define la hoja de propiedades secundaria que se creará. El receptor del mensaje debe liberar esta memoria con la [**función LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) cuando ya no sea necesaria.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**INFORMACIÓN DE PÁGINA DE DSA \_ SEC \_ \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

