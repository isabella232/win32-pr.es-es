---
description: Aplicación WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Aplicación WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659887"
---
# <a name="wpdservicesapisample-application"></a>Aplicación WpdServicesApiSample

Un servicio de dispositivo es una extensión de un objeto funcional: además de la Agrupación lógica de las capacidades del dispositivo, un servicio de dispositivo proporciona a las aplicaciones la capacidad de detectar dichas capacidades mediante programación.

La aplicación de ejemplo WpdServicesApiSample es una aplicación de escritorio de línea de comandos que puede usar para explorar los servicios de contactos en los dispositivos conectados al equipo. Puede explorar estos servicios mediante la lista de compatibles: formatos, eventos, métodos y servicios abstractos. También puede usar esta aplicación para recuperar las propiedades de un servicio de contacto determinado e invocar los métodos admitidos por ese servicio.

Si aún no tiene un dispositivo que admita servicios de contactos, puede ejecutar WpdServicesApiSample si instala por primera vez el WpdServiceSampleDriver que se incluye en el kit de controladores de Windows.

La aplicación de ejemplo WpdServicesApiSample incluye los siguientes archivos:



| **Archivo**                | **Descripción**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp  | Contiene métodos que enumeran el contenido de un servicio de contactos determinado.                                                                                                                                  |
| ContentProperties. cpp   | Contiene métodos que leen y escriben propiedades en un servicio de contactos determinado.                                                                                                                              |
| ServiceCapabilities. cpp | Contiene los métodos que recuperan los formatos admitidos, los eventos y los servicios abstractos admitidos por un servicio de contactos determinado.                                                                   |
| ServiceEnumeration. cpp  | Contiene las funciones auxiliares que recuperan información del dispositivo, como el nombre descriptivo del dispositivo o los servicios de contactos admitidos.                                                                       |
| ServiceMethods. cpp      | Contiene los métodos que recuperan e invocan los métodos admitidos por un servicio de contactos determinado.                                                                                                              |
| stdafx.cpp              | Incluye los archivos estándar.                                                                                                                                                                              |
| WpdServiceApiSample. cpp | Hospeda la función de inicio **\_ tmain** , que llama a la función local del **menú** , que muestra una lista de los dispositivos y las tareas disponibles y llama a la función adecuada para la selección del menú del usuario. |



 


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras](sample.md)
</dt> </dl>

 

 



