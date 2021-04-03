---
title: Etiqueta Vol
description: Etiqueta Vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075276"
---
# <a name="vol-tag"></a>Etiqueta Vol

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Establece el volumen de línea de base de la salida de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**\\Vol =***número***\\**



| Parte     | Descripción                                                         |
|----------|---------------------------------------------------------------------|
| *número* | Volumen de línea de base hablando: 0 es el silencio y 65535 es el volumen máximo. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

La configuración del volumen afecta a los canales izquierdo y derecho. No se puede establecer el volumen de cada canal por separado. Esta etiqueta solo se admite para la salida generada por TTS.

 

 




