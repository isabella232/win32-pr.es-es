---
title: método Unload
description: método Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790587"
---
# <a name="unload-method"></a>método Unload

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Descarga los datos de caracteres para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Characters. UNLOAD "*** CharacterID * *"**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Utilice este método cuando ya no necesite un carácter, para liberar memoria que se utiliza para almacenar información sobre el carácter. Si vuelve a tener acceso al carácter, utilice el método [**Load**](load-method.md) .

Este método no devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .

 

 