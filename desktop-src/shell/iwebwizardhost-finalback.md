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
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841876"
---
# <a name="webwizardhostfinalback-method"></a>Método WebWizardHost.FinalBack

Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Observaciones

Cuando el asistente muestra la primera página del  lado servidor y el usuario hace clic en el botón Atrás, el servidor invoca **FinalBack** cuando el controlador de eventos del cliente lo notifica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




