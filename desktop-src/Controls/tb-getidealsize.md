---
title: Mensaje de TB_GETIDEALSIZE (commctrl. h)
description: Obtiene el tamaño ideal de la barra de herramientas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078998"
---
# <a name="tb_getidealsize-message"></a>\_Mensaje GETIDEALSIZE TB

Obtiene el tamaño ideal de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Un **booleano** que indica si se va a recuperar el alto o ancho idóneos de la barra de herramientas. Use **true** para recuperar el alto ideal, **false** para recuperar el ancho ideal.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que recibe el alto o el ancho en el que se mostrarán todos los botones. Si *wParam* es **true**, solo el miembro **CY** (height) es válido. Si *wParam* es **false**, solo el miembro de **CX** (width) es válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

