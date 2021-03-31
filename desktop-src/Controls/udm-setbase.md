---
title: Mensaje de UDM_SETBASE (commctrl. h)
description: Establece la base de base de un control de flechas. El valor base determina si la ventana relacionada muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre están sin signo y los números decimales están firmados.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996716"
---
# <a name="udm_setbase-message"></a>\_Mensaje SETBASE UDM

Establece la base de base de un control de flechas. El valor base determina si la ventana relacionada muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre están sin signo y los números decimales están firmados.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo valor base para el control. Este parámetro puede ser 10 para decimal o 16 para hexadecimal.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el valor base anterior. Si se proporciona una base no válida, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





