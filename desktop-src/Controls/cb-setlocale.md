---
title: Mensaje de CB_SETLOCALE (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETLOCALE para establecer la configuración regional actual del cuadro combinado. Si el cuadro combinado tiene el \_ estilo de ordenación CBS y se agregan cadenas mediante CB \_ ADDSTRING, la configuración regional de un cuadro combinado afecta al modo en que se ordenan los elementos de la lista.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491542"
---
# <a name="cb_setlocale-message"></a>Mensaje de la \_ SETLOCALE CB

Una aplicación envía un mensaje **CB \_ SETLOCALE** para establecer la configuración regional actual del cuadro combinado. Si el cuadro combinado tiene el estilo de [**\_ ordenación CBS**](combo-box-styles.md) y se agregan cadenas mediante [**CB \_ ADDSTRING**](cb-addstring.md), la configuración regional de un cuadro combinado afecta al modo en que se ordenan los elementos de la lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador de configuración regional para el cuadro combinado que se va a usar para la ordenación al agregar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el identificador de configuración regional anterior. Si *wParam* especifica una configuración regional no instalada en el sistema, el valor devuelto es CB \_ Err y no se cambia la configuración regional del cuadro combinado actual.

## <a name="remarks"></a>Observaciones

Use la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir un identificador de configuración regional y la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) para construir un identificador de idioma. El identificador de idioma se compone de un identificador de idioma principal y un identificador de subidioma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**la de CB ( \_ GETLOCALE)**](cb-getlocale.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

