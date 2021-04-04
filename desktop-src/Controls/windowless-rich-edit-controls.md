---
title: Controles Rich Edit sin ventanas
description: Esta sección contiene información sobre los elementos de programación utilizados con controles Rich Edit sin ventana.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075326"
---
# <a name="windowless-rich-edit-controls"></a>Controles Rich Edit sin ventanas

Esta sección contiene información sobre los elementos de programación utilizados con controles Rich Edit sin ventana. El modelo de objetos componentes (COM) define un conjunto de interfaces para admitir objetos sin ventanas. Los objetos sin ventana pueden entrar en el estado activo en contexto sin tener su propia ventana, sino usar la ventana de su contenedor. Por lo tanto, un objeto sin ventana utiliza menos recursos del sistema y ofrece un mejor rendimiento a través de una activación y desactivación más rápidas. Además, los objetos sin ventana pueden ser no rectangulares y transparentes.

### <a name="overviews"></a>Temas de introducción



| Tema                                                                          | Contenido                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles de edición enriquecida sin ventanas](about-windowless-rich-edit-controls.md) | Un control Rich Edit sin ventana, también conocido como objeto de servicios de texto, es un objeto que proporciona la funcionalidad de un [control Rich Edit](rich-edit-controls.md) sin proporcionar la ventana.<br/> |



 

### <a name="functions"></a>Functions



| Tema                                            | Contenido                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | La función [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crea una instancia de un objeto de servicios de texto. El objeto servicios de texto admite una variedad de interfaces, entre las que se incluyen [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y el modelo de objetos de texto (Tom).<br/> |



 

### <a name="interfaces"></a>Interfaces



| Tema                                  | Contenido                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | Un objeto de servicios de texto usa la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) para obtener los servicios de host de texto.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Extiende el TOM para proporcionar una funcionalidad adicional para la operación sin ventanas.<br/>                                     |



 

 

 





