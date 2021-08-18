---
title: Propiedad DefaultCommand
description: Propiedad DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7aec703ffbabb98ae16609b0dcb01767fda5c38b42ed40f204e3a3bae5766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693640"
---
# <a name="defaultcommand-property"></a>Propiedad DefaultCommand

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el comando predeterminado del [**objeto Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.:Characters* *  **("**_CharacterID_*_"). Cadena Commands.DefaultCommand_* \[  =  \]



| Parte     | Descripción                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Valor de cadena que identifica el nombre (id.) del [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad le permite establecer un comando [**en**](/windows/desktop/lwef/the-command-object) la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) como el comando predeterminado y representarlo en negrita. Esto no cambia realmente el control de comandos ni los eventos de doble clic.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 