---
title: Mensaje de TB_HASACCELERATOR (commctrl. h)
description: Recupera un recuento de botones de la barra de herramientas que tienen el carácter de aceleración especificado.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR controles de mensajes de Windows
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
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490996"
---
# <a name="tb_hasaccelerator-message"></a>\_Mensaje HASACCELERATOR TB

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de. Es posible que este mensaje no se admita en versiones futuras de Windows.\]

Recupera un recuento de botones de la barra de herramientas que tienen el carácter de aceleración especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**WCHAR** que representa el carácter de acelerador de entrada que se va a probar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor **int** que recibe el número de botones que tienen el carácter de acelerador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

En primer lugar, el sistema consulta todos los botones de la barra de herramientas para los aceleradores coincidentes. Si no se encuentran coincidencias, el sistema envía la notificación [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) a la ventana primaria, solicitando el índice del botón que tiene el carácter de aceleración especificado. Si el elemento primario proporciona un índice, el recuento se establece en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





