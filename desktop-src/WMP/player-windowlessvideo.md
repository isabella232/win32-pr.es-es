---
title: Player.windowlessVideo
description: La propiedad windowlessVideo especifica o recupera un valor que indica si el control Reproductor de Windows Media representa vídeo en modo sin ventanas.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player.windowlessVideo Reproductor de Windows Media
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
ms.openlocfilehash: 733f8488d1d45f4c7e9794e64e2b3a70b41722048eac82d5d8eb6eb2f1d91cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572082"
---
# <a name="playerwindowlessvideo"></a>Player.windowlessVideo

La **propiedad windowlessVideo** especifica o recupera un valor que indica si el control Reproductor de Windows Media representa vídeo en modo sin ventanas.

## <a name="syntax"></a>Syntax

*player*. **windowlessVideo**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** que se especifica en tiempo de diseño y es de solo lectura a partir de entonces.



| Valor | Descripción                                      |
|-------|--------------------------------------------------|
| true  | El vídeo se representa en modo sin ventanas.        |
| false | Predeterminada. El vídeo se representa en modo de ventana. |



 

## <a name="remarks"></a>Comentarios

De forma predeterminada, un control Reproductor de Windows Media integrado representa el vídeo en su propia ventana dentro del área cliente. Cuando **windowlessVideo** está establecido en true, el control Player representa el vídeo directamente en el área de cliente, por lo que puede aplicar efectos especiales o agregar texto al vídeo.

En Windows Vista, la representación de vídeo en modo sin ventanas puede degradar el rendimiento.

La **propiedad windowlessVideo** no es compatible con Netscape Navigator. Establecer un valor para esta propiedad en Navigator puede producir resultados inesperados.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





