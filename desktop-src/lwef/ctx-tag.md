---
title: Etiqueta CTX
description: Etiqueta CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075962"
---
# <a name="ctx-tag"></a>Etiqueta CTX

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Establece el contexto del texto de salida.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

\\**CTX** = *cadena*\\



| Parte     | Descripción                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Cadena que especifica el contexto del texto que se muestra a continuación, que determina cómo se pronuncian los símbolos o las abreviaturas.<br/> **"Dirección"**    Direcciones o números de teléfono.<br/> **"Correo electrónico"**    Correo electrónico.<br/> Se desconoce el contexto **"desconocido"** (predeterminado).<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Esta etiqueta solo se admite para la salida generada por TTS. El intervalo de valores para el parámetro puede variar en función del motor TTS instalado.

 

 





