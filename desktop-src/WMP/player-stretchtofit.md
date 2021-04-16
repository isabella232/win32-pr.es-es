---
title: Player. stretchToFit
description: La propiedad stretchToFit especifica o recupera un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Media Player de Windows Player. stretchToFit
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708244"
---
# <a name="playerstretchtofit"></a>Player. stretchToFit

La propiedad **stretchToFit** especifica o recupera un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.

## <a name="syntax"></a>Sintaxis

*reproductor*. **stretchToFit**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de lectura/escritura.



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | El vídeo se ajustará para ajustarse a la ventana.              |
| false | Predeterminada. El vídeo no se ajustará para ajustarse a la ventana. |



 

## <a name="remarks"></a>Observaciones

Cuando **stretchToFit** se establece en true, el control de Media Player de Windows mantiene la relación de aspecto original del vídeo. Si la relación de aspecto del vídeo no coincide con la relación de aspecto de la ventana de vídeo, pueden aparecer áreas de máscara negra en la parte superior e inferior, o izquierda y derecha, de la imagen de vídeo.

Esta propiedad solo se aplica al control Media Player de Windows cuando se incrusta en una página web.

**Windows Media Player 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,1 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





