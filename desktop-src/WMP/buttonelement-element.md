---
title: Elemento BUTTONELEMENT
description: Elemento BUTTONELEMENT
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- Reproductor de Windows Media máscaras, elemento BUTTONELEMENT
- skins,BUTTONELEMENT, elemento
- Elemento BUTTONELEMENT
- referencia para máscaras, elemento BUTTONELEMENT
- elements,BUTTONELEMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889329"
---
# <a name="buttonelement-element"></a>Elemento BUTTONELEMENT

El **elemento BUTTONELEMENT** define un solo botón dentro de un **elemento BUTTONGROUP** primario. Admite los atributos siguientes. Los elementos **BUTTONELEMENT predefinidos** también se proporcionan para mayor comodidad.

El **elemento BUTTONELEMENT** admite los atributos siguientes.



| Atributo                                      | Descripción                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](buttonelement-cursor.md)             | Especifica o recupera el valor del cursor **BUTTONELEMENT** que aparece cuando el mouse está sobre **BUTTONELEMENT.**                                                                                      |
| [down](buttonelement-down.md)                 | Especifica o recupera el valor de arriba o abajo de **BUTTONELEMENT.**                                                                                                                                            |
| [downToolTip](buttonelement-downtooltip.md)   | Especifica o recupera el texto de la información sobre herramientas que aparece cuando el mouse está sobre **BUTTONELEMENT** y **buttonelement** está en estado de insanado.                                                                |
| [índice](buttonelement-index.md)               | Recupera el índice de **BUTTONELEMENT** dentro de **BUTTONGROUP**.                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | Especifica o recupera la clave de color que identifica este **BUTTONELEMENT** en el **grupo BUTTONELEMENT.**                                                                                                      |
| [Pegajoso](buttonelement-sticky.md)             | Especifica o recupera un valor que indica si **BUTTONELEMENT** es permanente. Cuando sea permanente, **buttonelement** cambiará los estados después de hacer clic y permanecerá en el nuevo estado hasta que se vuelva a hacer clic. |
| [upToolTip](buttonelement-uptooltip.md)       | Especifica o recupera el texto de información sobre herramientas que aparece cuando el mouse está sobre **BUTTONELEMENT** y **BUTTONELEMENT** está en estado activo o activo.                                                        |



 

El **elemento BUTTONELEMENT** admite el método siguiente.



| Método                           | Descripción                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [Haga clic](buttonelement-click.md) | Llama al **controlador de eventos onclick** definido para **BUTTONELEMENT.** |



 

El **elemento BUTTONELEMENT** puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [Controladores de eventos ambiente](ambient-event-handlers.md).

El **elemento BUTTONELEMENT** admite los siguientes atributos de ambiente: [enabled](ambientattributes-enabled.md) y [tabStop.](ambientattributes-tabstop.md)

Los efectos predefinidos son elementos **EFFECTS** normales con varias configuraciones de atributo comunes especificadas de forma predeterminada. Están disponibles los **siguientes elementos BUTTONELEMENT** predefinidos.



| BUTTONELEMENT predefinido         | Descripción                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [FFWDELEMENT](ffwdelement.md)   | BUTTONELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.fastForward**. |
| [NEXTELEMENT](nextelement.md)   | BUTTONELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.next.**        |
| [PAUSEELEMENT](pauseelement.md) | BUTTONELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.pause.**       |
| [PLAYELEMENT](playerelement.md) | BUTTONELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.play.**        |
| [PREVELEMENT](prevelement.md)   | ButtonELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.previous.**    |
| [REWELEMENT](rewelement.md)     | ButtonELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.rewind**.      |
| [STOPELEMENT](stopelement.md)   | BUTTONELEMENT **con** un controlador de eventos **onclick** integrado que llama a **player.controls.stop.**        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




