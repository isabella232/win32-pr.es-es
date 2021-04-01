---
title: Mensaje de TB_GETBITMAPFLAGS (commctrl. h)
description: Recupera las marcas que describen el tipo de mapa de bits que se va a utilizar.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151260"
---
# <a name="tb_getbitmapflags-message"></a>\_Mensaje GETBITMAPFLAGS TB

Recupera las marcas que describen el tipo de mapa de bits que se va a utilizar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que describe el tipo de mapa de bits que se debe usar. Si el valor devuelto tiene \_ establecida la marca grande TBBF, las aplicaciones deben usar mapas de bits grandes (24 x 24); de lo contrario, las aplicaciones deben usar mapas de bits pequeños (16 x 16). Todos los demás bits están reservados.

## <a name="remarks"></a>Observaciones

El valor devuelto por **TB \_ GETBITMAPFLAGS** solo es un aviso. El control de barra de herramientas recomienda mapas de bits grandes o pequeños en función de si el usuario ha elegido fuentes grandes o pequeñas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





