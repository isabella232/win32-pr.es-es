---
title: TB_MAPACCELERATOR mensaje (Commctrl.h)
description: Determina el identificador del botón que corresponde al carácter de acelerador especificado.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166689"
---
# <a name="tb_mapaccelerator-message"></a>Mensaje \_ MAPACCELERATOR de TB

Determina el identificador del botón que corresponde al carácter de acelerador especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Carácter de acelerador.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Puntero a un **objeto UINT.** En la devolución, si se realiza correctamente, este parámetro contendrán el identificador del botón que tiene *wParam* como carácter de acelerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si uno de los botones tiene *wParam* como carácter de acelerador o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) y **TB \_ MAPACCELECELECELERA** (ANSI)<br/>       |



 

 





