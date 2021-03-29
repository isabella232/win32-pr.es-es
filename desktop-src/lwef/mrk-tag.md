---
title: Etiqueta MRK
description: Etiqueta MRK
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776045"
---
# <a name="mrk-tag"></a>Etiqueta MRK

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Define un marcador en el texto hablado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**\\MRK =***número***\\**



| Parte     | Descripción                                        |
|----------|----------------------------------------------------|
| *número* | Valor entero largo que identifica el marcador. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Cuando el servidor procesa un marcador, genera un evento de marcador. Debe especificar un número mayor que cero (0) y distinto de 2147483647 o 2147483646.

 

 




