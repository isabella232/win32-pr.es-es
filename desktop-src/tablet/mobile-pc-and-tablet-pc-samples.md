---
description: Información general sobre los ejemplos de código de la interfaz de programación de aplicaciones (API) para las secciones de Tablet PC y Windows Touch del Windows SDK.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Ejemplos de tabletas y táctiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8562dcc1baa42f44d6ca675344d658b1bf693cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913549"
---
# <a name="tablet-and-touch-samples"></a>Ejemplos de tabletas y táctiles

Esta sección contiene ejemplos que muestran cómo se pueden desarrollar aplicaciones con C \# , Microsoft Visual Basic .net y C++ para trabajar con la entrada manuscrita y la entrada táctil.

De forma predeterminada, los ejemplos se instalan en <system drive> : \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ Samples \\ al instalar el SDK de Tablet PC.

> [!Note]  
> Al instalar el Windows SDK, el SDK de Windows Server o el SDK de .NET Framework, los ejemplos se instalan en la ruta de acceso predeterminada para ese SDK en particular.

 

## <a name="available-samples"></a>Ejemplos disponibles



| Muestra                                                                           | Descripción                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconocimiento avanzado](advanced-recognition-sample.md)                          | Muestra algunas de las características de reconocimiento más avanzadas, como la elección explícita del reconocedor, Factoids, etc.<br/>                                                                                                                                                             |
| [Formulario de notificaciones automáticas](auto-claims-form-sample.md)                                  | Muestra el uso de dos controles de entrada de lápiz: el control [InkEdit](/previous-versions/ms552265(v=vs.100)) y el control [InkPicture](/previous-versions/ms583740(v=vs.100)) .<br/>                                                                                                        |
| [Reconocimiento básico](basic-recognition-sample.md)                                | Muestra cómo compilar una aplicación sencilla de reconocimiento de escritura a mano mediante el objeto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) .<br/>                                                                                                                     |
| [Receptores de eventos de C++](c---event-sinks-sample.md)                                    | Muestra las plantillas de C++ para todos los eventos de la plataforma de tableta, que se pueden crear como subclases, copiar y pegar y usar como código de plantilla.<br/>                                                                                                                                   |
| [Autocompletar caracteres](character-autocomplete-sample.md)                      | Muestra cómo implementar la función autocompletar de caracteres en japonés mediante el uso de las API de reconocimiento.<br/>                                                                                                                                                                                 |
| [Ejemplo de blog de Ink Web](ink-blog-web-sample.md)                                   | Muestra cómo crear un control de usuario administrado que tiene la funcionalidad de entrada manuscrita y hospeda ese control en Internet Explorer.<br/>                                                                                                                                                         |
| [Portapapeles de tinta](ink-clipboard-sample.md)                                        | Muestra la interoperabilidad de entradas manuscritas mediante el portapapeles.<br/>                                                                                                                                                                                                                          |
| [Colección de entradas manuscritas](ink-collection-sample.md)                                      | Muestra una aplicación de Windows Forms simple que utiliza el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para recopilar la entrada de lápiz.<br/>                                                                                                                                     |
| [Divisor de tinta](ink-divider-sample.md)                                            | Muestra cómo utilizar el objeto [divisor](/previous-versions/ms839398(v=msdn.10)) para realizar el análisis de tinta.<br/>                                                                                                                                                                            |
| [Borrado de tinta](ink-erasing-sample.md)                                            | Muestra la eliminación de trazos de tinta en una aplicación de Windows Forms que usa el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para recopilar la entrada manuscrita.<br/>                                                                                                             |
| [Prueba de posicionamiento de tinta](ink-hit-test-sample.md)                                          | Muestra dos maneras de la entrada manuscrita de la prueba de posicionamiento.<br/>                                                                                                                                                                                                                                       |
| [Reconocimiento de tinta](ink-recognition-sample.md)                                    | Muestra cómo puede compilar una aplicación sencilla de reconocimiento de escritura a mano.<br/>                                                                                                                                                                                                    |
| [Serialización de tinta](ink-serialization-sample.md)                                | Muestra cómo serializar la entrada de lápiz en el formato serializado de tinta (ISF).<br/>                                                                                                                                                                                                           |
| [Ejemplo de control Web de entrada manuscrita](ink-web-control-sample.md)                             | Muestra cómo crear un control de entrada de lápiz para su uso en un explorador Web.<br/>                                                                                                                                                                                                             |
| [Zoom de tinta](ink-zoom-sample.md)                                                  | Muestra cómo aplicar un zoom adecuado a la entrada de lápiz en una aplicación.<br/>                                                                                                                                                                                                                        |
| [Ejemplo de varios reconocedores](multiple-recognizers-sample.md)                   | Muestra cómo seleccionar entre varios reconocedores instalados y, a continuación, usar el reconocedor seleccionado.<br/>                                                                                                                                                                        |
| [Ejemplo de Web de implementación sin interacción](no-touch-deployment-web-sample.md)             | Muestra cómo usar el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para que la entrada de texto en las aplicaciones de formularios sea más sencilla. Extiende el ejemplo de formulario de notificaciones automáticas.<br/>                                                                                      |
| [PenInputPanel](peninputpanel-sample.md)                                        | Muestra cómo usar el objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para que la entrada de texto en las aplicaciones de formularios sea más sencilla. Extiende el ejemplo de formulario de notificaciones automáticas.<br/>                                                                                      |
| [Ejemplo de colección de tintas RealTimeStylus](realtimestylus-ink-collection-sample.md) | Muestra la colección de tintas mediante RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Ejemplo de complemento RealTimeStylus](realtimestylus-plug-in-sample.md)               | Muestra cómo trabajar con RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Ejemplo de formulario de papel digitalizado](scanned-paper-form-sample.md)                       | Muestra el uso de un formulario examinado como un mapa de bits y se especifica como imagen de fondo de un control [InkPicture](/previous-versions/ms583740(v=vs.100)) en la parte superior de un formulario. Se han habilitado varias regiones para la colección de tinta (o, especificada como "inkable").<br/> |
| [Ejemplo de información de plataforma de Tablet PC](tablet-pc-platform-info-sample.md)             | Muestra el uso de la función de la API de Windows GetSystemMetrics () para determinar si la aplicación se ejecuta en un Tablet PC.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Plantilla de ejemplo de DLL de reconocedor](recognizer-dll-sample-template.md)
</dt> </dl>

 

