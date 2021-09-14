---
title: Count (propiedad)
description: Count (propiedad)
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072389"
---
# <a name="count-property"></a>Count (propiedad)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un entero Long (propiedad de solo lectura) que especifica el recuento de objetos [**Command**](/windows/desktop/lwef/the-command-object) en la [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Count_*

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Count** incluye solo el número de [**objetos Command**](/windows/desktop/lwef/the-command-object) que defina en la [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) No se incluyen las entradas de servidor u otras entradas de cliente.

 

 