---
title: CB_SETITEMDATA mensaje (Winuser.h)
description: Una aplicación envía un mensaje \_ CB SETITEMDATA para establecer el valor asociado al elemento especificado en un cuadro combinado.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170117"
---
# <a name="cb_setitemdata-message"></a>Mensaje \_ DE CB SETITEMDATA

Una aplicación envía un **mensaje \_ CB SETITEMDATA** para establecer el valor asociado al elemento especificado en un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el nuevo valor que se va a asociar al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es CB \_ ERR.

## <a name="remarks"></a>Observaciones

Si el elemento especificado está en un cuadro combinado dibujado por el propietario creado sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) este mensaje reemplaza el valor del parámetro *lParam* del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) que agregó el elemento al cuadro combinado.

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

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





