---
title: WM_ADSPROP_SHEET_CREATE mensaje
description: Se envía al objeto de notificación para crear una hoja de propiedades secundaria en Active Directory complemento MMC.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ec88eaed682fd16fecb717b851b902d5ba52ce08d5360aa78b881a4b8cb4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024203"
---
# <a name="wm_adsprop_sheet_create-message"></a>Mensaje \_ CREATE de WM ADSPROP \_ SHEET \_

El **mensaje \_ WM ADSPROP SHEET \_ \_ CREATE** se envía al objeto de notificación para crear una hoja de propiedades secundaria en un Active Directory complemento MMC.

> [!Note]  
> Este valor de mensaje no se define en un archivo de encabezado publicado. Para usar este valor de mensaje, debe definirlo usted mismo en el formato exacto que se muestra.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador del objeto de notificación. Para obtener este identificador, llame [**a ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntero a una estructura DE INFORMACIÓN DE PÁGINA de [**DSA \_ SEC \_ \_**](dsa-sec-page-info.md) que define la página secundaria que se creará. Solo se puede crear una hoja de propiedades secundaria con el mensaje **WM \_ ADSPROP \_ SHEET \_ CREATE,** por lo que la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) solo puede contener una [**estructura DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa. Debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto para este mensaje siempre es cero.

## <a name="remarks"></a>Comentarios

El autor de la llamada debe asignar la estructura PAGE INFO de [**DSA \_ \_ \_ SEC,**](dsa-sec-page-info.md) la cadena de título y todas las cadenas [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) mediante una sola llamada a la [**función LocalAlloc.**](/windows/desktop/api/winbase/nf-winbase-localalloc) El **mensaje CREATE de WM \_ ADSPROP SHEET \_ \_ es** un mensaje asincrónico, por lo que devolverá antes de que se cree la hoja secundaria. Por este problema, la memoria debe permanecer intacta después de que se devuelva el mensaje. El receptor liberará esta memoria con una sola llamada a la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) después de crear la hoja secundaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**INFORMACIÓN DE PÁGINA DE DSA \_ \_ \_ SEC**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

