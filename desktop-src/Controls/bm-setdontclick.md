---
title: Mensaje de BM_SETDONTCLICK (Winuser. h)
description: Establece una marca en un botón de radio que controla la generación de \_ mensajes clics de BN cuando el botón recibe el foco.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656494"
---
# <a name="bm_setdontclick-message"></a>\_Mensaje SETDONTCLICK de BM

Establece una marca en un botón de radio que controla la generación de mensajes [ \_ clics de BN](bn-clicked.md) cuando el botón recibe el foco.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Un **booleano** que especifica el estado. **True** para establecer la marca; de lo contrario, **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





