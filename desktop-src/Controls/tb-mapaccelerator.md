---
title: Mensaje de TB_MAPACCELERATOR (commctrl. h)
description: Determina el identificador del botón que corresponde al carácter de acelerador especificado.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803145"
---
# <a name="tb_mapaccelerator-message"></a>\_Mensaje MAPACCELERATOR TB

Determina el identificador del botón que corresponde al carácter de acelerador especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Carácter de acelerador.

</dd> <dt>

*lParam* \[ enuncia\]
</dt> <dd>

Puntero a un **uint**. En la devolución, si se realiza correctamente, este parámetro contendrá el identificador del botón que tiene *wParam* como carácter de aceleración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si uno de los botones tiene *wParam* como carácter de acelerador o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) y **TB \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





