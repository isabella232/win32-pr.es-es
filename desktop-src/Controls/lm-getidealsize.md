---
title: Mensaje de LM_GETIDEALSIZE (commctrl. h)
description: Recupera el alto preferido de un vínculo para el ancho actual del control.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489100"
---
# <a name="lm_getidealsize-message"></a>\_Mensaje GETIDEALSIZE de LM

Recupera el alto preferido de un vínculo para el ancho actual del control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Ancho máximo del vínculo, en píxeles.</dd> <dt>

*lParam* \[ enuncia\]
</dt> <dd>Cuando este mensaje vuelve, contiene un puntero a una estructura de <a href="/previous-versions//dd145106(v=vs.85)">**tamaño**</a> . El miembro **CY** de esta estructura indica el alto ideal del control para el ancho especificado. Ajusta el miembro de **CX** a la cantidad de espacio realmente necesaria.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Entero que representa el alto preferido del texto del vínculo, en píxeles.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

