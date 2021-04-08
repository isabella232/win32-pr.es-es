---
title: Propiedad Count
description: Propiedad Count
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904541"
---
# <a name="count-property"></a>Propiedad Count

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un entero largo (propiedad de solo lectura) que especifica el recuento de objetos de [**comando**](/windows/desktop/lwef/the-command-object) en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Commands. Count**

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Count** incluye solo el número de objetos de [**comando**](/windows/desktop/lwef/the-command-object) que se definen en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . No se incluyen las entradas de servidor o de otro cliente.

 

 