---
title: TB_INSERTMARKHITTEST mensaje (Commctrl.h)
description: Recupera la información de marca de inserción para un punto de una barra de herramientas.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166722"
---
# <a name="tb_insertmarkhittest-message"></a>Mensaje \_ INSERTMARKHITTEST de TB

Recupera la información de marca de inserción para un punto de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura POINT que**](/previous-versions//dd162805(v=vs.85)) contiene las coordenadas de la prueba de acceso, en relación con el área de cliente de la barra de herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recibe la información de la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el punto es una marca de inserción o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

