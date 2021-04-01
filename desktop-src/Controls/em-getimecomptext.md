---
title: Mensaje EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera el texto de composición del editor de métodos de entrada (IME).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996749"
---
# <a name="em_getimecomptext-message"></a>\_Mensaje GETIMECOMPTEXT em

Recupera el texto de composición del editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estructura [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .

</dd> <dt>

*lParam* 
</dt> <dd>

Búfer que recibe el texto de la composición. El tamaño de este búfer está incluido en el miembro **CB** de la estructura *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el valor devuelto es el número de caracteres Unicode copiados en el búfer. De lo contrario, es cero.

## <a name="remarks"></a>Observaciones

Este mensaje solo toma cadenas Unicode.

**Advertencia de seguridad:** Asegúrese de tener un búfer suficiente para el tamaño de la entrada. Si no lo hace, podrían producirse problemas en la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





