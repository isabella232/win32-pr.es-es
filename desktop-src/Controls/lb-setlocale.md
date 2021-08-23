---
title: LB_SETLOCALE mensaje (Winuser.h)
description: Establece la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo SORT de LBS) y del texto agregado por el \_ mensaje \_ ADDSTRING de LB.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623b8550b3d5f382ddc8ccc1e1cfcf861a2f8c0a7877ba60c57e393abc1401d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958544"
---
# <a name="lb_setlocale-message"></a>Mensaje \_ SETLOCALE de LB

Establece la configuración regional actual del cuadro de lista. Puede usar la configuración regional para determinar el criterio de ordenación correcto del texto mostrado (para los cuadros de lista con el estilo [**\_ SORT de LBS)**](list-box-styles.md) y del texto agregado por el [**mensaje \_ ADDSTRING de LB.**](lb-addstring.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador de configuración regional que el cuadro de lista usará para ordenar al agregar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el identificador de configuración regional anterior. Si el *parámetro wParam* especifica una configuración regional que no está instalada en el sistema, el valor devuelto es LB ERR y la configuración regional del cuadro de lista actual \_ no cambia.

## <a name="remarks"></a>Comentarios

Use la [**macro MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir un identificador de configuración regional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETLOCALE**](lb-getlocale.md)
</dt> </dl>

 

