---
title: Mensaje EM_SETPALETTE (RichEdit. h)
description: Cambia la paleta que un control Rich Edit utiliza para la ventana de presentación.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079272"
---
# <a name="em_setpalette-message"></a>\_Mensaje SETPALETTE em

Cambia la paleta que un control Rich Edit utiliza para la ventana de presentación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la nueva paleta utilizada por el control Rich Edit.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El control Rich Edit no comprueba si la nueva paleta es válida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





