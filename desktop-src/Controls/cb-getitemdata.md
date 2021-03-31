---
title: Mensaje de CB_GETITEMDATA (Winuser. h)
description: Una aplicación envía un \_ mensaje CB GETITEMDATA a un cuadro combinado para recuperar el valor proporcionado por la aplicación asociado al elemento especificado en el cuadro combinado.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802240"
---
# <a name="cb_getitemdata-message"></a>\_Mensaje GETITEMDATA CB

Una aplicación envía un mensaje **CB \_ GETITEMDATA** a un cuadro combinado para recuperar el valor proporcionado por la aplicación asociado al elemento especificado en el cuadro combinado.

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

El valor devuelto es el valor asociado al elemento. Si se produce un error, es CB \_ error.

Si el elemento está en un cuadro combinado dibujado por el propietario creado sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el valor devuelto es el valor contenido en el parámetro *lParam* del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) , que agregó el elemento al cuadro combinado. Si no se usó el estilo **CBS \_ HASSTRINGS** , el valor devuelto es el parámetro *lParam* contenido en un mensaje [**\_ SETITEMDATA de CB**](cb-setitemdata.md) .

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

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**CB \_ SETITEMDATA**](cb-setitemdata.md)
</dt> </dl>

 

 





