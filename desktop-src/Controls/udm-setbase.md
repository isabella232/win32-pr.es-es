---
title: UDM_SETBASE mensaje (Commctrl.h)
description: Establece la base base de base para un control de flechas. El valor base determina si la ventana de compañeros muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre son sin signo y los números decimales están firmados.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165489"
---
# <a name="udm_setbase-message"></a>Mensaje \_ SETBASE de UDM

Establece la base base de base para un control de flechas. El valor base determina si la ventana de compañeros muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre son sin signo y los números decimales están firmados.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo valor base para el control. Este parámetro puede ser 10 para decimal o 16 para hexadecimal.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el valor base anterior. Si se especifica una base no válida, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





