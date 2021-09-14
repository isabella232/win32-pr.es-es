---
title: EM_GETIMECOMPTEXT mensaje (Richedit.h)
description: Recupera el texto de composición del Editor de métodos de entrada (IME).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892321"
---
# <a name="em_getimecomptext-message"></a>Mensaje \_ EM GETIMECOMPTEXT

Recupera el texto de composición del Editor de métodos de entrada (IME).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estructura [**IMECOMPTEXT.**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)

</dd> <dt>

*lParam* 
</dt> <dd>

Búfer que recibe el texto de composición. El tamaño de este búfer se encuentra en el miembro **cb** de la *estructura wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el valor devuelto es el número de caracteres Unicode copiados en el búfer. De lo contrario, es cero.

## <a name="remarks"></a>Observaciones

Este mensaje solo toma cadenas Unicode.

**Advertencia de seguridad:** Asegúrese de tener un búfer suficiente para el tamaño de la entrada. Si no lo hace, podría causar problemas en la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





