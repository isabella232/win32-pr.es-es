---
description: Introducción a los ejemplos de código de la interfaz de programación de aplicaciones (API) para tablet PC y Windows Touch del SDK Windows.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Ejemplos táctiles y de tableta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cf87ca2cc35da58fe05a72436288413af9f72ecff63a1b2418fb071ca5a025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449788"
---
# <a name="tablet-and-touch-samples"></a>Ejemplos táctiles y de tableta

Esta sección contiene ejemplos que muestran cómo se pueden desarrollar aplicaciones con C, Microsoft Visual Basic .NET y C++ para trabajar con entrada de lápiz \# y entrada táctil.

De forma predeterminada, los ejemplos se instalan en : Archivos de programa <system drive> Microsoft Tablet PC Platform SDK Samples al instalar el SDK de Tablet \\ \\ \\ \\ PC.

> [!Note]  
> Al instalar el SDK Windows, el SDK de Windows Server o el SDK de .NET Framework, los ejemplos se instalan en la ruta de acceso predeterminada para ese SDK concreto.

 

## <a name="available-samples"></a>Ejemplos disponibles



| Muestra                                                                           | Descripción                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconocimiento avanzado](advanced-recognition-sample.md)                          | Muestra algunas de las características de reconocimiento más avanzadas, como la elección explícita del reconocedor, factoids y mucho más.<br/>                                                                                                                                                             |
| [Formulario de notificaciones automáticas](auto-claims-form-sample.md)                                  | Muestra el uso de dos controles de entrada de lápiz: el control [InkEdit](/previous-versions/ms552265(v=vs.100)) y el control [InkPicture.](/previous-versions/ms583740(v=vs.100))<br/>                                                                                                        |
| [Reconocimiento básico](basic-recognition-sample.md)                                | Muestra cómo crear una aplicación de reconocimiento de escritura a mano simple mediante el [objeto RecognizerContext.](/previous-versions/ms828542(v=msdn.10))<br/>                                                                                                                     |
| [Receptores de eventos de C++](c---event-sinks-sample.md)                                    | Muestra plantillas en C++ para todos los eventos de la plataforma de tabletas, que se pueden crear subclases o copiar y pegar y usar como código de plantilla.<br/>                                                                                                                                   |
| [Autocompletar de caracteres](character-autocomplete-sample.md)                      | Muestra cómo implementar la función Autocompletar de caracteres en japonés mediante las API de reconocimiento.<br/>                                                                                                                                                                                 |
| [Ejemplo web de blog de Ink](ink-blog-web-sample.md)                                   | Muestra cómo crear un control de usuario administrado que tenga capacidad de invocación y host que controle en Internet Explorer<br/>                                                                                                                                                         |
| [Portapapeles de Ink](ink-clipboard-sample.md)                                        | Muestra la interoperabilidad de entrada manuscrita mediante el Portapapeles.<br/>                                                                                                                                                                                                                          |
| [Colección de entrada de lápiz](ink-collection-sample.md)                                      | Muestra una aplicación de Windows aplicación de formulario simple que usa el [objeto InkCollector](/previous-versions/ms583683(v=vs.100)) para recopilar la entrada de lápiz.<br/>                                                                                                                                     |
| [Divisor de entrada de lápiz](ink-divider-sample.md)                                            | Muestra cómo usar el objeto [Divider](/previous-versions/ms839398(v=msdn.10)) para realizar análisis de entrada de lápiz.<br/>                                                                                                                                                                            |
| [Borrado de entrada de lápiz](ink-erasing-sample.md)                                            | Muestra la eliminación de trazos de entrada de lápiz Windows aplicación de formulario que usa el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para recopilar la entrada de lápiz.<br/>                                                                                                             |
| [Prueba de impacto de entrada manuscrita](ink-hit-test-sample.md)                                          | Muestra dos maneras de probar la entrada de lápiz.<br/>                                                                                                                                                                                                                                       |
| [Reconocimiento de entrada de lápiz](ink-recognition-sample.md)                                    | Muestra cómo puede crear una aplicación de reconocimiento de escritura a mano sencilla.<br/>                                                                                                                                                                                                    |
| [Serialización de entrada de lápiz](ink-serialization-sample.md)                                | Muestra cómo serializar la entrada de lápiz al formato serializado de entrada de lápiz (ISF).<br/>                                                                                                                                                                                                           |
| [Ejemplo de control web ink](ink-web-control-sample.md)                             | Muestra cómo crear un control Ink para usarlo en un explorador web.<br/>                                                                                                                                                                                                             |
| [Zoom de entrada manuscrita](ink-zoom-sample.md)                                                  | Muestra cómo acercar correctamente la entrada de lápiz en una aplicación.<br/>                                                                                                                                                                                                                        |
| [Ejemplo de varios reconocedores](multiple-recognizers-sample.md)                   | Muestra cómo seleccionar entre una variedad de reconocedores instalados y, a continuación, usar el reconocedor seleccionado.<br/>                                                                                                                                                                        |
| [Ejemplo web de implementación no táctil](no-touch-deployment-web-sample.md)             | Muestra cómo usar el objeto [PenInputPanel para](/previous-versions/aa514041(v=msdn.10)) facilitar la entrada de texto en las aplicaciones de formularios. Extiende el ejemplo de formulario notificaciones automáticas.<br/>                                                                                      |
| [PenInputPanel](peninputpanel-sample.md)                                        | Muestra cómo usar el objeto [PenInputPanel para](/previous-versions/aa514041(v=msdn.10)) facilitar la entrada de texto en las aplicaciones de formularios. Extiende el ejemplo de formulario notificaciones automáticas.<br/>                                                                                      |
| [Ejemplo de colección de lápiz De RealTimeStylus](realtimestylus-ink-collection-sample.md) | Muestra la colección de entrada de lápiz mediante RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Ejemplo del complemento RealTimeStylus](realtimestylus-plug-in-sample.md)               | Muestra cómo trabajar con RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Ejemplo de formulario de papel digitalizado](scanned-paper-form-sample.md)                       | Muestra el uso de un formulario examinado en como mapa de bits y especificado como imagen de fondo para un control [InkPicture](/previous-versions/ms583740(v=vs.100)) sobre la parte superior de un formulario. Se han habilitado varias regiones para la colección de entrada de lápiz (o , especificadas como "inkable").<br/> |
| [Ejemplo de información de la plataforma de Tablet PC](tablet-pc-platform-info-sample.md)             | Muestra el uso de la función de API GetSystemMetrics() Windows para determinar si la aplicación se ejecuta en un tablet PC.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Plantilla de ejemplo de DLL de Recognizer](recognizer-dll-sample-template.md)
</dt> </dl>

 

