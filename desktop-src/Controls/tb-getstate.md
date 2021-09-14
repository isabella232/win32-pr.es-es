---
title: TB_GETSTATE mensaje (Commctrl.h)
description: Recupera información sobre el estado del botón especificado en una barra de herramientas, como si está habilitado, presionado o activado.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166765"
---
# <a name="tb_getstate-message"></a>Mensaje \_ GETSTATE de TB

Recupera información sobre el estado del botón especificado en una barra de herramientas, como si está habilitado, presionado o activado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón para el que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la información de estado del botón si se realiza correctamente o -1 en caso contrario. La información de estado del botón puede ser una combinación de los valores enumerados en Estados del [**botón de la**](toolbar-button-states.md)barra de herramientas .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





