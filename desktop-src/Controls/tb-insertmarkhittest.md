---
title: Mensaje de TB_INSERTMARKHITTEST (commctrl. h)
description: Recupera la información de la marca de inserción para un punto de una barra de herramientas.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079196"
---
# <a name="tb_insertmarkhittest-message"></a>\_Mensaje INSERTMARKHITTEST TB

Recupera la información de la marca de inserción para un punto de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que contiene las coordenadas de la prueba de posicionamiento, en relación con el área cliente de la barra de herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recibe la información de la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el punto es una marca de inserción o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

