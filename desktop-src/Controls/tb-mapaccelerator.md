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
ms.openlocfilehash: f905ccf5ea01e3c06cb87a160a44598c2c4a7790c972f4ee83b245e3ed5c0111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168089"
---
# <a name="tb_mapaccelerator-message"></a>MENSAJE \_ MAPACCELERATOR DE TB

Determina el identificador del botón que corresponde al carácter de acelerador especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Carácter de acelerador.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Puntero a **un UINT.** En la devolución, si se realiza correctamente, este parámetro contendrán el identificador del botón que tiene *wParam* como carácter de acelerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si uno de los botones tiene *wParam* como carácter de acelerador o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) y **TB \_ MAPACCELECELECELERA** (ANSI)<br/>       |



 

 





