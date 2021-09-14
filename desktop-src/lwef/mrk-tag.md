---
title: Etiqueta Mrk
description: Etiqueta Mrk
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168262"
---
# <a name="mrk-tag"></a>Etiqueta Mrk

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Define un marcador en el texto hablado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**\\ Mrk=**_number_*_\\_*



| Parte     | Descripción                                        |
|----------|----------------------------------------------------|
| *número* | Valor entero Long que identifica el marcador. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Cuando el servidor procesa un marcador, genera un evento de marcador. Debe especificar un número mayor que cero (0) y no igual a 2147483647 o 2147483646.

 

 




