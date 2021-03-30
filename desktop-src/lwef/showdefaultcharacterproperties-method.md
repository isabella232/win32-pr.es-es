---
title: Método ShowDefaultCharacterProperties
description: Método ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775450"
---
# <a name="showdefaultcharacterproperties-method"></a>Método ShowDefaultCharacterProperties

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Muestra las propiedades del carácter predeterminado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente * * *. ShowDefaultCharacterProperties* *  \[ *X* , *y*\]



| Parte | Descripción                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Opcional. Valor entero corto que indica la coordenada de pantalla horizontal (*X* ) para mostrar la ventana. Esta coordenada debe especificarse en píxeles. |
| *S*  | Opcional. Valor entero corto que indica la coordenada de pantalla vertical (*Y*) para mostrar la ventana. Esta coordenada debe especificarse en píxeles.    |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al llamar a este método se muestra la ventana Propiedades de carácter predeterminado (no la hoja de propiedades agente de Microsoft). Si no especifica las coordenadas X e y, la ventana aparecerá en la última ubicación en la que se mostró.

## <a name="see-also"></a>Consulte también

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




