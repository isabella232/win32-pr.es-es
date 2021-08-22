---
description: Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.
title: Método WebWizardHost.FinalBack (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 0338b20023fda059a5205c9a42a7b7d669c5554d5fca878fcb8904c807ceceae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092612"
---
# <a name="webwizardhostfinalback-method"></a>Método WebWizardHost.FinalBack

Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Comentarios

Cuando el asistente muestra la primera página del  lado servidor y el usuario hace clic en el botón Atrás, el servidor invoca **FinalBack** cuando el controlador de eventos del cliente lo notifica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




