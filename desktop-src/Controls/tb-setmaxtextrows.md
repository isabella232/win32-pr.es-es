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
ms.openlocfilehash: 1d6a1e1a2cda7b3dced4cf538623578d48b41d38925629f2985a35974baed229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167485"
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

## <a name="remarks"></a>Comentarios

Para que el texto se ajuste, debe establecer el ancho máximo del botón mediante el envío de un mensaje [**\_ SETBUTTONWIDTH de TB.**](tb-setbuttonwidth.md) El texto se ajusta en un salto de palabra; se omiten los saltos de línea (" \\ n") del texto. El texto de las barras de herramientas \_ TBSTYLE LIST siempre se muestra en una sola línea.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





