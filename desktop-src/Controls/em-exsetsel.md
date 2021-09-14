---
title: EM_EXSETSEL mensaje (Richedit.h)
description: Selecciona un intervalo de caracteres o objetos del Modelo de objetos componentes (COM) en un control Edición enriquección enriquecte de Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255626"
---
# <a name="em_exsetsel-message"></a>Mensaje \_ EM EXSETSEL

Selecciona un intervalo de caracteres o objetos del Modelo de objetos componentes (COM) en un control Edición enriquección enriquecte de Microsoft.

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





