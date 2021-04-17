---
title: Player. windowlessVideo
description: La propiedad windowlessVideo especifica o recupera un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Media Player de Windows Player. windowlessVideo
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708755"
---
# <a name="playerwindowlessvideo"></a>Player. windowlessVideo

La propiedad **windowlessVideo** especifica o recupera un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.

## <a name="syntax"></a>Sintaxis

*reproductor*. **windowlessVideo**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** que se especifica en tiempo de diseño y, a partir de ese momento, es de solo lectura.



| Value | Descripción                                      |
|-------|--------------------------------------------------|
| true  | El vídeo se representa en el modo sin ventanas.        |
| false | Predeterminada. El vídeo se representa en modo de ventana. |



 

## <a name="remarks"></a>Observaciones

De forma predeterminada, un control incrustado de Windows Media Player representa el vídeo en su propia ventana dentro del área cliente. Cuando **windowlessVideo** se establece en true, el control Player representa el vídeo directamente en el área cliente, por lo que puede aplicar efectos especiales o capas el vídeo con texto.

En Windows Vista, la representación de vídeo en el modo sin ventanas puede degradar el rendimiento.

La propiedad **windowlessVideo** no es compatible con Netscape Navigator. Establecer un valor para esta propiedad en el navegador puede producir resultados inesperados.

**Windows Media Player 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





