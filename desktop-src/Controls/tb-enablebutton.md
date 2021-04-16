---
title: Mensaje de TB_ENABLEBUTTON (commctrl. h)
description: Habilita o deshabilita el botón especificado en una barra de herramientas.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- TB_ENABLEBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658403"
---
# <a name="tb_enablebutton-message"></a>\_Mensaje ENABLEBUTTON TB

Habilita o deshabilita el botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón que se va a habilitar o deshabilitar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **booleano** que indica si se debe habilitar o deshabilitar el botón especificado. Si es **true**, el botón está habilitado. Si es **false**, el botón está deshabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se ha habilitado un botón, se puede presionar y activar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

