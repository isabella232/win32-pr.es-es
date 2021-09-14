---
description: Aplicación WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Aplicación WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262036"
---
# <a name="wpdapisample-application"></a>Aplicación WpdApiSample

La aplicación de ejemplo WpdApiSample es una aplicación de escritorio de línea de comandos que permite enumerar dispositivos conectados, explorar dispositivos, consultar objetos para propiedades y atributos, enviar y recuperar objetos, entre otros. Al iniciarse, la aplicación abre una ventana de comandos que enumera las tareas que puede realizar.

La aplicación de ejemplo WpdApiSample incluye los siguientes archivos:



| **Archivo**               | **Descripción**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration.cpp | Contiene funciones que enumeran todos los objetos de un dispositivo.                                                                                                                                            |
| ContentProperties.cpp  | Contiene funciones que leen y escriben propiedades de objeto y que hacen solicitudes masivas de establecimiento y obtención de propiedades.                                                                                                         |
| ContentTransfer.cpp    | Contiene funciones que transfieren contenido hacia o desde el dispositivo, leen los requisitos de tipo de objeto y crean una carpeta en el dispositivo.                                                                         |
| DeviceCapabilities.cpp | Contiene funciones para enumerar los tipos de objetos funcionales en el dispositivo, enumerar los tipos de contenido admitidos por cada tipo de objeto funcional y mostrar perfiles de objeto de representación.                             |
| DeviceEnumeration.cpp  | Enumera los nombres descriptivos, los fabricantes y las descripciones de todos los dispositivos conectados.                                                                                                                       |
| DeviceEvents.cpp       | Contiene funciones que registra eventos de dispositivo y sus parámetros cada vez que se desencadenan eventos.                                                                                                                 |
| stdafx.cpp             | Incluye los archivos estándar.                                                                                                                                                                              |
| WpdApiSample.cpp       | Hospeda la función de inicio **\_ tmain,** que llama a la función **DoMenu** local, que muestra una lista de dispositivos y tareas disponibles y llama a la función adecuada para la selección de menú del usuario. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo](sample.md)
</dt> </dl>

 

 



