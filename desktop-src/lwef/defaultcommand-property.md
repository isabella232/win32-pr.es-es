---
title: Propiedad DefaultCommand
description: Propiedad DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077677"
---
# <a name="defaultcommand-property"></a>Propiedad DefaultCommand

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el comando predeterminado del objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

Caracteres del agente *. * * ** *  **("***CharacterID***"). Commands. DefaultCommand** ( \[  =  *cadena* )\]



| Parte     | Descripción                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Un valor de cadena que identifica el nombre (ID.) del [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad permite establecer un [**comando**](/windows/desktop/lwef/the-command-object) en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) como el comando predeterminado, para representarlo en negrita. Esto no cambia realmente el control de comandos ni los eventos de doble clic.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 