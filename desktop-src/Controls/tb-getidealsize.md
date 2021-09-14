---
title: TB_GETIDEALSIZE mensaje (Commctrl.h)
description: Obtiene el tamaño ideal de la barra de herramientas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166821"
---
# <a name="tb_getidealsize-message"></a>Mensaje \_ DE TB GETIDEALSIZE

Obtiene el tamaño ideal de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Valor **BOOL que** indica si se debe recuperar el alto o ancho ideal de la barra de herramientas. Use **TRUE** para recuperar el alto ideal, **FALSE,** para recuperar el ancho ideal.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) que recibe el alto o ancho en el que se mostrarían todos los botones. Si *wParam es* **TRUE,** solo el **miembro cy** (alto) es válido. Si *wParam es* **FALSE,** solo el **miembro cx** (ancho) es válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

