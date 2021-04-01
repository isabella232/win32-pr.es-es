---
title: Mensaje EM_GETIMECOLOR (RichEdit. h)
description: Recupera el color de composición del editor de métodos de entrada (IME).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996750"
---
# <a name="em_getimecolor-message"></a>\_Mensaje GETIMECOLOR em

Recupera el color de composición del editor de métodos de entrada (IME).

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0. No se admite en las versiones posteriores de Rich Edit.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Matriz de cuatro elementos de estructuras [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que recibe el color de la composición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





