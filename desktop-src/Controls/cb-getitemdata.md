---
title: CB_GETITEMDATA mensaje (Winuser.h)
description: Una aplicación envía un mensaje CB GETITEMDATA a un cuadro combinado para recuperar el valor proporcionado por la aplicación asociado al elemento especificado \_ en el cuadro combinado.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062540"
---
# <a name="cb_getitemdata-message"></a>Mensaje \_ GETITEMDATA de CB

Una aplicación envía un **mensaje \_ CB GETITEMDATA** a un cuadro combinado para recuperar el valor proporcionado por la aplicación asociado al elemento especificado en el cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El índice de base cero de un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el valor asociado al elemento. Si se produce un error, es CB \_ ERR.

Si el elemento está en un cuadro combinado dibujado por el propietario creado sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) el valor devuelto es el valor contenido en el parámetro *lParam* del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING,**](cb-insertstring.md) que agregó el elemento al cuadro combinado. Si no se usó el estilo **\_ HASSTRINGS de CBS,** el valor devuelto es el parámetro *lParam* contenido en un [**mensaje \_ SETITEMDATA de CB.**](cb-setitemdata.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**CB \_ SETITEMDATA**](cb-setitemdata.md)
</dt> </dl>

 

 





