---
title: Mensaje de SB_SETICON (commctrl. h)
description: Establece el icono de un elemento en una barra de estado.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905456"
---
# <a name="sb_seticon-message"></a>\_Mensaje SETICON de SB

Establece el icono de un elemento en una barra de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que recibirá el icono. Si este parámetro es-1, se supone que la barra de estado es una barra de estado simple.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del icono que se va a establecer. Si este valor es **null**, el icono se quita del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

La barra de estado no destruirá el icono. Es responsabilidad de la aplicación que realiza la llamada realizar un seguimiento de los iconos y destruirlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





