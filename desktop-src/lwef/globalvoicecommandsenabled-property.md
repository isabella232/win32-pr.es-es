---
title: Propiedad GlobalVoiceCommandsEnabled
description: Propiedad GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f889d242afca406ba443fd3d9a19afb837fbed0390f5c0c3d2bbd2ac2ccbccb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751449"
---
# <a name="globalvoicecommandsenabled-property"></a>Propiedad GlobalVoiceCommandsEnabled

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si la voz está habilitada para los comandos globales del Agente .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). Commands.GlobalVoiceCommandsEnabled_*

\[ = *Booleana*\]



| Parte      | Descripción                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que indica si los parámetros de voz para los comandos globales del Agente están habilitados. **Los parámetros** de voz True (valor predeterminado) están habilitados. <br/> **False** Los parámetros de voz están deshabilitados.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Microsoft Agent agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana Comandos de voz y para mostrar y ocultar el carácter. Si establece **GlobalVoiceCommandsEnabled** en **False,** el Agente deshabilita los parámetros de voz [](caption-property.md) para estos comandos, así como los parámetros de voz para el título de los objetos [**Commands de**](/windows/desktop/lwef/the-commands-collection-object) otro cliente. Esto le permite eliminarlos de la gramática activa actual del cliente. Sin embargo, dado que esto podría bloquear el acceso de voz a otros clientes, restablezca esta propiedad a **True** después de procesar la entrada de voz del usuario.

Deshabilitar la propiedad no afecta al menú emergente del carácter. Los comandos globales agregados por el servidor seguirán apareciendo. No se pueden quitar del menú emergente.

 

