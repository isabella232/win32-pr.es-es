---
title: PlayerApplication.hasDisplay
description: La propiedad hasDisplay recupera un valor que indica si el vídeo puede mostrarse a través del control de reproductor remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Windows Media Player
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
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708752"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

La propiedad **hasDisplay** recupera un valor que indica si el vídeo puede mostrarse a través del control de reproductor remoto.

## <a name="syntax"></a>Sintaxis

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de solo lectura.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se usa cuando la comunicación remota del control de Media Player de Windows.

Varios controles de Windows Media Player se pueden ejecutar de forma remota al mismo tiempo, pero el vídeo solo puede mostrarse en una ubicación a la vez, ya sea en el modo completo del reproductor o en uno de los controles de Windows Media Player remotos. Utilice esta propiedad para determinar si el control actual es el que se puede mostrar en el vídeo.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





