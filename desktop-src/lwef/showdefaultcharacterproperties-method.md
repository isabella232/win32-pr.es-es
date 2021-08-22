---
title: ShowDefaultCharacterProperties (método)
description: ShowDefaultCharacterProperties (método)
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d19f92f555038fe4c13c7a752d49bf35a04b70964f6110d881976af3e72a8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746311"
---
# <a name="showdefaultcharacterproperties-method"></a>ShowDefaultCharacterProperties (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Muestra las propiedades del carácter predeterminado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent,. ShowDefaultCharacterProperties* *  \[ *X* , *Y*\]



| Parte | Descripción                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Opcional. Valor entero corto que indica la coordenada de pantalla horizontal *(X)* para mostrar la ventana. Esta coordenada debe especificarse en píxeles. |
| *S*  | Opcional. Valor entero corto que indica la coordenada de pantalla vertical *(Y)* para mostrar la ventana. Esta coordenada debe especificarse en píxeles.    |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al llamar a este método se muestra la ventana de propiedades de caracteres predeterminada (no la hoja de propiedades de Microsoft Agent). Si no especifica las coordenadas X e Y, la ventana aparece en la última ubicación en la que se mostró.

## <a name="see-also"></a>Consulte también

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




