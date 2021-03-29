---
title: BUTTONELEMENT (elemento)
description: BUTTONELEMENT (elemento)
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- Aspectos de Windows Media Player, elemento BUTTONELEMENT
- máscaras, elemento BUTTONELEMENT
- BUTTONELEMENT (elemento)
- referencia de las máscaras, elemento BUTTONELEMENT
- elementos, BUTTONELEMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777461"
---
# <a name="buttonelement-element"></a>BUTTONELEMENT (elemento)

El elemento **BUTTONELEMENT** define un solo botón dentro de un elemento **BUTTONGROUP** primario. Admite los siguientes atributos. Los elementos **BUTTONELEMENT** predefinidos también se proporcionan por comodidad.

El elemento **BUTTONELEMENT** admite los siguientes atributos.



| Atributo                                      | Descripción                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](buttonelement-cursor.md)             | Especifica o recupera el valor del cursor **ButtonElement** que aparece cuando el mouse está sobre **BUTTONELEMENT**.                                                                                      |
| [vertical](buttonelement-down.md)                 | Especifica o recupera el valor hacia arriba o hacia abajo de **BUTTONELEMENT**.                                                                                                                                            |
| [downToolTip](buttonelement-downtooltip.md)   | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre **BUTTONELEMENT** y **ButtonElement** está en estado inactivo.                                                                |
| [índice](buttonelement-index.md)               | Recupera el índice de **BUTTONELEMENT** dentro de **BUTTONGROUP**.                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | Especifica o recupera la clave del color que identifica este **BUTTONELEMENT** en el grupo **ButtonElement** .                                                                                                      |
| [rápidas](buttonelement-sticky.md)             | Especifica o recupera un valor que indica si **BUTTONELEMENT** es permanente. Cuando sea persistente, un **BUTTONELEMENT** cambiará de estado después de hacer clic en él y permanecerá en el nuevo estado hasta que se vuelva a hacer clic. |
| [Información sobre herramientas](buttonelement-uptooltip.md)       | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre **BUTTONELEMENT** y **ButtonElement** está en estado activo o activo.                                                        |



 

El elemento **BUTTONELEMENT** admite el método siguiente.



| Método                           | Descripción                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [hizo](buttonelement-click.md) | Llama al controlador de eventos **onclick** definido para **BUTTONELEMENT**. |



 

El elemento **BUTTONELEMENT** puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [controladores de eventos ambiente](ambient-event-handlers.md).

El elemento **BUTTONELEMENT** admite los siguientes atributos de ambiente: [Enabled](ambientattributes-enabled.md) y [tabStop](ambientattributes-tabstop.md).

Los efectos predefinidos son elementos de **efectos** normales con varios valores de atributos comunes especificados de forma predeterminada. Están disponibles los siguientes elementos **BUTTONELEMENT** predefinidos.



| BUTTONELEMENT predefinido         | Descripción                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [FFWDELEMENT](ffwdelement.md)   | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. fastForward**. |
| [NEXTELEMENT](nextelement.md)   | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. Next**.        |
| [PAUSEELEMENT](pauseelement.md) | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. PAUSE**.       |
| [PLAYELEMENT](playerelement.md) | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. Play**.        |
| [PREESTADO](prevelement.md)   | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. Previous**.    |
| [REWELEMENT](rewelement.md)     | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. Rewind**.      |
| [STOPELEMENT](stopelement.md)   | **BUTTONELEMENT** con un controlador de eventos **onclick** integrado que llama a **Player. Controls. Stop**.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




