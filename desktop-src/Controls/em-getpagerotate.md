---
title: Mensaje EM_GETPAGEROTATE (RichEdit. h)
description: Obtiene el diseño de texto de un control Rich Edit de Microsoft.
ms.assetid: 0efb112e-ad51-4ebb-9037-3aee3ab9ad1d
keywords:
- EM_GETPAGEROTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7bc7cd3c77ae88cd4c8710e14b4472e57407ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492485"
---
# <a name="em_getpagerotate-message"></a>\_Mensaje GETPAGEROTATE em

\[**Em \_ GETPAGEROTATE** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Obtiene el diseño de texto de un control Rich Edit de Microsoft.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Obtiene el diseño del texto actual. Para obtener una lista de posibles valores de diseño de texto, consulte [**em \_ SETPAGEROTATE**](em-setpagerotate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETPAGEROTATE em**](em-setpagerotate.md)
</dt> </dl>

 

 





