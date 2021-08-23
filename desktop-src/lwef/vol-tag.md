---
title: Etiqueta Vol
description: Etiqueta Vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d03b7bb536ada8dc783e1506ba4bedfd54c6b5698e1aa68dfe55fd1f939d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035983"
---
# <a name="vol-tag"></a>Etiqueta Vol

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Establece el volumen de habla de línea de base de la salida de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**\\ Vol=**_number_*_\\_*



| Parte     | Descripción                                                         |
|----------|---------------------------------------------------------------------|
| *número* | Volumen de habla de línea base: 0 es silencio y 65535 es el volumen máximo. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

La configuración del volumen afecta a los canales izquierdo y derecho. No se puede establecer el volumen de cada canal por separado. Esta etiqueta solo se admite para la salida generada por TTS.

 

 




