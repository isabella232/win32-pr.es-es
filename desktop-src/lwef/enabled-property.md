---
title: Propiedad Enabled (objeto Balloon)
description: Propiedad Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695824"
---
# <a name="enabled-property-balloon-object"></a>Propiedad Enabled (objeto Balloon)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve si el globo de palabras está habilitado para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Globo. Enabled_*



| Value     | Descripción              |
|-----------|--------------------------|
| **True**  | El globo está habilitado.  |
| **False** | El globo está deshabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **Enabled** devuelve un valor booleano que especifica si el globo está habilitado. El estado predeterminado de globo de palabras se establece como parte de la definición de un carácter cuando el carácter se compila en el editor de caracteres del agente de Microsoft. Si se define un carácter para que no admita el globo de palabras, esta propiedad siempre será **false** para el carácter.

 

 




