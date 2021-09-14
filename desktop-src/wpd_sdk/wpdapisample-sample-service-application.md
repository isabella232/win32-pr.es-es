---
description: Aplicación WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Aplicación WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247023"
---
# <a name="wpdservicesapisample-application"></a>Aplicación WpdServicesApiSample

Un servicio de dispositivo es una extensión de un objeto funcional: además de agrupar lógicamente las funcionalidades del dispositivo, un servicio de dispositivo proporciona a las aplicaciones la capacidad de detectar esas funcionalidades mediante programación.

La aplicación de ejemplo WpdServicesApiSample es una aplicación de escritorio de línea de comandos que puede usar para explorar los servicios de contactos en dispositivos conectados al equipo. Puede explorar estos servicios enumerando los formatos, eventos, métodos y servicios abstractos admitidos. También puede usar esta aplicación para recuperar las propiedades de un servicio Contact determinado e invocar métodos compatibles con ese servicio.

Si aún no tiene un dispositivo que admita los servicios contacts, puede ejecutar WpdServicesApiSample si primero instala wpdServiceSampleDriver que se incluye en el kit de controladores de Windows.

La aplicación de ejemplo WpdServicesApiSample incluye los siguientes archivos:



| **Archivo**                | **Descripción**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration.cpp  | Contiene métodos que enumeran el contenido de un servicio Contacts determinado.                                                                                                                                  |
| ContentProperties.cpp   | Contiene métodos que leen y escriben propiedades en un servicio Contacts determinado.                                                                                                                              |
| ServiceCapabilities.cpp | Contiene los métodos que recuperan los formatos, eventos y servicios abstractos admitidos por un servicio Contacts determinado.                                                                   |
| ServiceEnumeration.cpp  | Contiene las funciones auxiliares que recuperan información del dispositivo, como el nombre descriptivo del dispositivo o los servicios de contactos compatibles.                                                                       |
| ServiceMethods.cpp      | Contiene los métodos que recuperan e invocan métodos admitidos por un servicio Contacts determinado.                                                                                                              |
| stdafx.cpp              | Incluye los archivos estándar.                                                                                                                                                                              |
| WpdServiceApiSample.cpp | Hospeda la función de inicio **\_ tmain,** que llama a la función **DoMenu** local, que muestra una lista de dispositivos y tareas disponibles y llama a la función adecuada para la selección de menú del usuario. |



 


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras](sample.md)
</dt> </dl>

 

 



