---
title: Mensaje WM_DSA_SHEET_CREATE_NOTIFY
description: Publicado en el complemento MMC de Active Directory para crear una hoja de propiedades secundaria.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996470"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>\_Creación de \_ mensaje \_ de \_ notificación de hoja DSA de WM

La **hoja de datos DSA de WM crear mensaje de \_ \_ \_ \_ notificación** se publica en el complemento MMC de Active Directory para crear una hoja de propiedades secundaria.

> [!Note]  
> Este valor de mensaje no está definido en un archivo de encabezado publicado. Para usar este valor de mensaje, debe definirlo en el formato exacto que se muestra.

 


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

*identificador* 
</dt> <dd>

Identificador de ventana de la ventana del complemento que procesará este mensaje. Este identificador se obtiene del miembro **hwndHidden** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntero a una estructura de [**\_ información de \_ página \_ de DSA sec**](dsa-sec-page-info.md) que define la hoja de propiedades secundaria que se va a crear. El receptor del mensaje debe liberar esta memoria con la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) cuando ya no sea necesaria.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**información de página de DSA \_ s \_ \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

