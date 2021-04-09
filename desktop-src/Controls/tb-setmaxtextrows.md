---
title: Mensaje de TB_SETMAXTEXTROWS (commctrl. h)
description: Establece el número máximo de filas de texto que se muestran en un botón de la barra de herramientas.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996110"
---
# <a name="tb_setmaxtextrows-message"></a>\_Mensaje SETMAXTEXTROWS TB

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

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Para hacer que el texto se ajuste, debe establecer el ancho máximo del botón mediante el envío de un mensaje de [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) . El texto se ajusta en un salto de palabra; \\se omiten los saltos de línea ("n") en el texto. El texto de las \_ barras de herramientas de la lista TBSTYLE siempre se muestra en una sola línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





