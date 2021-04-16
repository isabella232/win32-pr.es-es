---
title: Mensaje WM_DSA_SHEET_CLOSE_NOTIFY
description: Se publica en el complemento MMC de Active Directory cuando se destruye una hoja de propiedades secundaria.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658217"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>\_Mensaje de \_ \_ notificación de cierre de hoja DSA de WM \_

El mensaje de **\_ notificación de \_ \_ cierre \_ de hoja DSA de WM** se envía al complemento MMC de Active Directory cuando se destruye una hoja de propiedades secundaria.

> [!Note]  
> Este valor de mensaje no está definido en un archivo de encabezado publicado. Para usar este valor de mensaje, debe definirlo en el formato exacto que se muestra.

 


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

*identificador* 
</dt> <dd>

Identificador de ventana de la ventana del complemento que procesará este mensaje. Este identificador se obtiene del miembro **hwndHidden** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un valor de 32 bits definido por la aplicación. Esto se obtiene del miembro **wParamSheetClose** de la estructura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 





