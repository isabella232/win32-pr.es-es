---
title: PlayerApplication.hasDisplay
description: La propiedad hasDisplay recupera un valor que indica si el vídeo se puede mostrar a través del control Player remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication.hasDisplay Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cffddc08c154ced6d7cb72b18642b5ebb4960e539e5682d1cf6e8518b74831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747364"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

La **propiedad hasDisplay** recupera un valor que indica si el vídeo se puede mostrar a través del control Player remoto.

## <a name="syntax"></a>Syntax

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de solo **lectura.**

## <a name="remarks"></a>Comentarios

Esta propiedad solo se usa al usar la comunicación remota Reproductor de Windows Media control .

Varios Reproductor de Windows Media pueden ejecutarse de forma remota al mismo tiempo, pero el vídeo solo se puede mostrar en una ubicación a la vez, ya sea en el modo completo del reproductor o en uno de los controles Reproductor de Windows Media remotos. Use esta propiedad para determinar si el control actual es el a través del cual se puede mostrar el vídeo.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve **true.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





