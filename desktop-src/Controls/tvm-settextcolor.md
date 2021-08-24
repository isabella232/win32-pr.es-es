---
title: TVM_SETTEXTCOLOR mensaje (Commctrl.h)
description: Establece el color del texto del control. Puede enviar este mensaje explícitamente o mediante la macro \_ TreeView SetTextColor.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41559abd6724ee9c8ce9f86cfcff092ad13d949a80a55d45ff996f36b284932d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503615"
---
# <a name="tvm_settextcolor-message"></a>Mensaje \_ SETTEXTCOLOR de TVM

Establece el color del texto del control. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView SetTextColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que contiene el nuevo color de texto. Si este argumento es -1, el control volverá a usar el color del sistema para el color del texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor COLORREF** que representa el color de texto anterior. Si este valor es -1, el control usaba el color del sistema para el color del texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

