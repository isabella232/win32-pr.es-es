---
title: Controles de edición enriquecciones sin ventanas
description: Esta sección contiene información sobre los elementos de programación usados con controles de edición enriquecciones sin ventanas.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165249"
---
# <a name="windowless-rich-edit-controls"></a>Controles de edición enriquecciones sin ventanas

Esta sección contiene información sobre los elementos de programación usados con controles de edición enriquecciones sin ventanas. El modelo de objetos componentes (COM) define un conjunto de interfaces para admitir objetos sin ventana. Los objetos sin ventana pueden entrar en el estado activo local sin tener su propia ventana, sino usar la ventana de su contenedor. Por lo tanto, un objeto sin ventanas usa menos recursos del sistema y proporciona un mejor rendimiento a través de una activación y desactivación más rápidas. Además, los objetos sin ventana pueden ser no rectangulares y transparentes.

### <a name="overviews"></a>Temas de introducción



| Tema                                                                          | Contenido                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles Rich Edit sin ventanas](about-windowless-rich-edit-controls.md) | Un control de edición enriquecido sin ventanas, también conocido como objeto de servicios de texto, es un objeto que proporciona la funcionalidad de un [control](rich-edit-controls.md) de edición enriquecido sin proporcionar la ventana.<br/> |



 

### <a name="functions"></a>Functions



| Tema                                            | Contenido                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | La [**función CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crea una instancia de un objeto de servicios de texto. El objeto de servicios de texto admite una variedad de interfaces, como [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) y Text Object Model (TOM).<br/> |



 

### <a name="interfaces"></a>Interfaces



| Tema                                  | Contenido                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | Un objeto de servicios de texto usa la interfaz [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) para obtener servicios host de texto.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Extiende el TOM para proporcionar funcionalidad adicional para el funcionamiento sin ventanas.<br/>                                     |



 

 

 





