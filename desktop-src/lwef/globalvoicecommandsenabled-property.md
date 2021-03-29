---
title: Propiedad GlobalVoiceCommandsEnabled
description: Propiedad GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995265"
---
# <a name="globalvoicecommandsenabled-property"></a>Propiedad GlobalVoiceCommandsEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si la voz está habilitada para los comandos globales del agente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*directivas. ***Caracteres ("*** CharacterID * *"). Commands. GlobalVoiceCommandsEnabled**

\[ = *booleano*\]



| Parte      | Descripción                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que indica si están habilitados los parámetros de voz para los comandos globales del agente. **True** (valor predeterminado) los parámetros de voz están habilitados. <br/> **False** Los parámetros de voz están deshabilitados.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El agente de Microsoft agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana comandos de voz y para mostrar y ocultar el carácter. Si establece **GlobalVoiceCommandsEnabled** en **false**, el agente deshabilita los parámetros de voz para estos comandos, así como los parámetros de voz para el [**título**](caption-property.md) de los objetos de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de otros clientes. Esto le permite eliminarlos de la gramática activa actual del cliente. Sin embargo, dado que esto potencialmente bloquea el acceso de voz a otros clientes, restablezca esta propiedad en **true** después de procesar la entrada de voz del usuario.

Deshabilitar la propiedad no afecta al menú emergente del carácter. Los comandos globales agregados por el servidor seguirán apareciendo. No se pueden quitar del menú emergente.

 

