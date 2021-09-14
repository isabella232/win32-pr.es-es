---
title: TB_SETMAXTEXTROWS mensaje (Commctrl.h)
description: Establece el número máximo de filas de texto que se muestran en un botón de la barra de herramientas.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166585"
---
# <a name="tb_setmaxtextrows-message"></a>Mensaje \_ SETMAXTEXTROWS de TB

Establece el número máximo de filas de texto que se muestran en un botón de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de filas de texto que se pueden mostrar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Para que el texto se ajuste, debe establecer el ancho máximo del botón mediante el envío de un mensaje [**\_ SETBUTTONWIDTH de TB.**](tb-setbuttonwidth.md) El texto se ajusta en un salto de palabra; se omiten los saltos de \\ línea ("n") del texto. El texto de las barras de herramientas \_ TBSTYLE LIST siempre se muestra en una sola línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





