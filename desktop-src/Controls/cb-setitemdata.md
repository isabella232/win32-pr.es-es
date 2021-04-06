---
title: Mensaje de CB_SETITEMDATA (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETITEMDATA para establecer el valor asociado al elemento especificado en un cuadro combinado.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905408"
---
# <a name="cb_setitemdata-message"></a>\_Mensaje SETITEMDATA CB

Una aplicación envía un mensaje **CB \_ SETITEMDATA** para establecer el valor asociado al elemento especificado en un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice basado en cero del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el nuevo valor que se va a asociar al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es CB \_ error.

## <a name="remarks"></a>Observaciones

Si el elemento especificado se encuentra en un cuadro combinado dibujado por el propietario creado sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , este mensaje reemplaza el valor del parámetro *lParam* del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) que agregó el elemento al cuadro combinado.

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

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





