---
title: Mensaje de TB_GETSTATE (commctrl. h)
description: Recupera información sobre el estado del botón especificado en una barra de herramientas, como, por ejemplo, si está habilitado, presionado o activado.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905081"
---
# <a name="tb_getstate-message"></a>\_Mensaje GETSTATE TB

Recupera información sobre el estado del botón especificado en una barra de herramientas, como, por ejemplo, si está habilitado, presionado o activado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón para el que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la información de estado del botón si se realiza correctamente, o-1 en caso contrario. La información sobre el estado de los botones puede ser una combinación de los valores que aparecen en [**los Estados**](toolbar-button-states.md)de los botones de la barra de herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





