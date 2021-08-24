---
title: TB_HASACCELERATOR mensaje (Commctrl.h)
description: Recupera un recuento de botones de barra de herramientas que tienen el carácter de acelerador especificado.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420f06e71c6920c266c96d8b2580549fa0eaace2bd3abdd37524502d4039aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078289"
---
# <a name="tb_hasaccelerator-message"></a>Mensaje \_ HASACCELERATOR de TB

\[Destinado a uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Recupera un recuento de botones de barra de herramientas que tienen el carácter de acelerador especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

WCHAR **que representa** el carácter del acelerador de entrada que se debe probar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un **valor int** que recibe el número de botones que tienen el carácter de acelerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

El uso de este mensaje puede poner en peligro la seguridad del programa.

## <a name="remarks"></a>Comentarios

En primer lugar, el sistema consulta todos los botones de la barra de herramientas para buscar aceleradores que coincidan. Si no se encuentra ninguna coincidencia, el sistema envía la notificación [ \_ MAPACCELERATOR](tbn-mapaccelerator.md) de TBN a la ventana primaria, solicitando el índice del botón que tiene el carácter de acelerador especificado. Si el elemento primario proporciona un índice, el recuento se establece en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





