---
description: Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.
title: Método WebWizardHost. FinalBack (Shldisp. h)
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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910458"
---
# <a name="webwizardhostfinalback-method"></a>WebWizardHost. FinalBack, método

Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Observaciones

Cuando el asistente muestra la primera página del servidor y el usuario hace clic en el botón **atrás** , el servidor invoca **FinalBack** cuando el controlador de eventos del cliente notifica ese evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




