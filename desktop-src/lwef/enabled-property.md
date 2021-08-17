---
title: Propiedad Enabled (objeto Balloon)
description: Obtenga información sobre la propiedad del objeto Globo habilitado. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d4eaa09e173d847e9dead1bbd559b59e2d12a2d40b5f1d1f989d3cf70263ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752007"
---
# <a name="enabled-property-balloon-object"></a>Propiedad Enabled (objeto Balloon)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve si el globo de palabras está habilitado para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Balloon.Enabled_*



| Valor     | Descripción              |
|-----------|--------------------------|
| **True**  | El globo está habilitado.  |
| **False** | El globo está deshabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad Enabled** devuelve un valor booleano que especifica si el globo está habilitado. El estado predeterminado del globo de palabras se establece como parte de la definición de un carácter cuando el carácter se compila en el Editor de caracteres de Microsoft Agent. Si se define un carácter para no admitir la palabra globo, esta propiedad siempre será **False** para el carácter.

 

 




