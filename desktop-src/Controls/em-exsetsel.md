---
title: Mensaje EM_EXSETSEL (RichEdit. h)
description: Selecciona un intervalo de caracteres o objetos del modelo de objetos componentes (COM) en un control Rich Edit de Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905368"
---
# <a name="em_exsetsel-message"></a>\_Mensaje EXSETSEL em

Selecciona un intervalo de caracteres o objetos del modelo de objetos componentes (COM) en un control Rich Edit de Microsoft.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que especifica el intervalo de selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la selección que se establece realmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





