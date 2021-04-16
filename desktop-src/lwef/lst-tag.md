---
title: Etiqueta lst
description: Etiqueta lst
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532133"
---
# <a name="lst-tag"></a>Etiqueta lst

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Repite la última instrucción oral del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

\\**LST**\\

</dd> </dl>

### <a name="remarks"></a>Observaciones

Esta etiqueta permite que un carácter repita su última instrucción oral. Esta etiqueta debe aparecer por sí misma en el método [**Speak**](speak-method.md) ; no se puede incluir ningún otro texto o parámetro. Cuando se repite el texto hablado, cualquier otra etiqueta incluida en el texto original se repite, excepto para los marcadores. Cualquier. WAV y. Los archivos LWV incluidos en el texto también se repiten.

 

 




