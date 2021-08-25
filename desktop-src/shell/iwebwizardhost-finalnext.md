---
description: Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.
title: Método WebWizardHost.FinalNext (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: a694ced28663a005bfdacd406adb3f6b3d6cd0300db2a101c9fdee4bf215a23d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821125"
---
# <a name="webwizardhostfinalnext-method"></a>Método WebWizardHost.FinalNext

Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Comentarios

Cuando el asistente muestra la última página HTML del  lado  servidor y el usuario hace clic en el botón Siguiente o Finalizar, el servidor invoca **FinalNext** en el controlador de eventos de ese botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




