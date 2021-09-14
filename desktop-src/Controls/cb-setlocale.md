---
title: CB_SETLOCALE mensaje (Winuser.h)
description: Una aplicación envía un mensaje \_ CB SETLOCALE para establecer la configuración regional actual del cuadro combinado. Si el cuadro combinado tiene el estilo SORT de CBS y las cadenas se agregan mediante CB ADDSTRING, la configuración regional de un cuadro combinado afecta a cómo se ordenan los elementos \_ \_ de lista.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170109"
---
# <a name="cb_setlocale-message"></a>Mensaje \_ SETLOCALE de CB

Una aplicación envía un **mensaje \_ CB SETLOCALE** para establecer la configuración regional actual del cuadro combinado. Si el cuadro combinado tiene el estilo SORT de [**CBS \_**](combo-box-styles.md) y las cadenas se agregan mediante [**CB \_ ADDSTRING,**](cb-addstring.md)la configuración regional de un cuadro combinado afecta a cómo se ordenan los elementos de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador de configuración regional del cuadro combinado que se usará para la ordenación al agregar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el identificador de configuración regional anterior. Si *wParam especifica* una configuración regional no instalada en el sistema, el valor devuelto es CB ERR y la configuración regional del cuadro combinado actual \_ no cambia.

## <a name="remarks"></a>Observaciones

Use la [**macro MAKELCID para**](/windows/desktop/api/winnt/nf-winnt-makelcid) construir un identificador de configuración regional y la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) para construir un identificador de idioma. El identificador de idioma se forma de un identificador de idioma principal y un identificador de sublenguaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETLOCALE**](cb-getlocale.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

