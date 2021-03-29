---
description: Aplicación WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Aplicación WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809536"
---
# <a name="wpdapisample-application"></a>Aplicación WpdApiSample

La aplicación de ejemplo WpdApiSample es una aplicación de escritorio de línea de comandos que permite enumerar dispositivos conectados, explorar dispositivos, consultar objetos para propiedades y atributos, enviar y recuperar objetos, etc. Al iniciarse, la aplicación abre una ventana de comandos que enumera las tareas que puede realizar.

La aplicación de ejemplo WpdApiSample incluye los siguientes archivos:



| **Archivo**               | **Descripción**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp | Contiene funciones que enumeran todos los objetos de un dispositivo.                                                                                                                                            |
| ContentProperties. cpp  | Contiene funciones que leen y escriben propiedades de objeto y hacen solicitudes set/get de propiedad masivas.                                                                                                         |
| ContentTransfer. cpp    | Contiene funciones que transfieren contenido hacia o desde el dispositivo, leen los requisitos de tipo de objeto y crean una carpeta en el dispositivo.                                                                         |
| DeviceCapabilities. cpp | Contiene funciones para enumerar los tipos de objeto funcional en el dispositivo, enumerar los tipos de contenido admitidos por cada tipo de objeto funcional y mostrar los perfiles de objeto de representación.                             |
| DeviceEnumeration. cpp  | Enumera los nombres descriptivos, los fabricantes y las descripciones de todos los dispositivos conectados.                                                                                                                       |
| DeviceEvents. cpp       | Contiene funciones que registran eventos de dispositivo y sus parámetros cada vez que se activan eventos.                                                                                                                 |
| stdafx.cpp             | Incluye los archivos estándar.                                                                                                                                                                              |
| WpdApiSample. cpp       | Hospeda la función de inicio **\_ tmain** , que llama a la función local del **menú** , que muestra una lista de los dispositivos y las tareas disponibles y llama a la función adecuada para la selección del menú del usuario. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo](sample.md)
</dt> </dl>

 

 



