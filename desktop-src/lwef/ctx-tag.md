---
title: Etiqueta Ctx
description: Etiqueta Ctx
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072383"
---
# <a name="ctx-tag"></a>Etiqueta Ctx

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Establece el contexto del texto de salida.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

\\**Ctx** = *cadena*\\



| Parte     | Descripción                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Cadena que especifica el contexto del texto siguiente, que determina cómo se pronuncian los símbolos o las abreviaturas.<br/> **"Dirección"**    Direcciones o números de teléfono.<br/> **"Correo electrónico"**    Correo electrónico.<br/> Se desconoce el contexto **"Desconocido"** (valor predeterminado).<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Esta etiqueta solo se admite para la salida generada por TTS. El intervalo de valores del parámetro puede variar en función del motor de TTS instalado.

 

 





