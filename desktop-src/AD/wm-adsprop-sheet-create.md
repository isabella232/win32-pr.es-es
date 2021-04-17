---
title: Mensaje WM_ADSPROP_SHEET_CREATE
description: Se envía al objeto de notificación para crear una hoja de propiedades secundaria en un complemento MMC de Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534222"
---
# <a name="wm_adsprop_sheet_create-message"></a>\_ \_ Crear mensaje de hoja de ADSPROP de WM \_

El mensaje de creación de la hoja de ADSPROP de WM se envía al objeto de notificación para crear una hoja de propiedades secundaria en un complemento de MMC de Active Directory. **\_ \_ \_**

> [!Note]  
> Este valor de mensaje no está definido en un archivo de encabezado publicado. Para usar este valor de mensaje, debe definirlo en el formato exacto que se muestra.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador del objeto de notificación. Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntero a una estructura de [**\_ información de \_ página \_ de DSA sec**](dsa-sec-page-info.md) que define la página secundaria que se va a crear. Solo se puede crear una hoja de propiedades secundaria con **la \_ hoja de ADSPROP de WM \_ \_ Create** Message, por lo que la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) solo puede contener una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza. Debe ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto para este mensaje es siempre cero.

## <a name="remarks"></a>Observaciones

El autor de la llamada debe asignar la estructura de [**información de página de DSA \_ \_ \_ sec**](dsa-sec-page-info.md) , la cadena de título y todas las cadenas de [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) con una sola llamada a la función [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) . El mensaje de creación de la **\_ \_ hoja \_ ADSPROP de WM** es un mensaje asincrónico, por lo que se devolverá antes de crear la hoja secundaria. Por este motivo, la memoria debe permanecer intacta después de que el mensaje se devuelva. El receptor liberará esta memoria con una sola llamada a la función [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) una vez creada la hoja secundaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**información de página de DSA \_ s \_ \_**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

