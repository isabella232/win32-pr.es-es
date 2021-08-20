---
title: Descargar arquitectura del administrador
description: Descargar arquitectura del administrador
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Reproductor de Windows Media en línea,Download Manager
- online stores,Download Manager
- tipo 2 tiendas en línea, Administrador de descarga
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
- arquitectura del Administrador de descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae04be86d935f87202abe4b0bf73e833a9da07cf89526b9dcb60de31eb881a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997105"
---
# <a name="download-manager-architecture"></a>Descargar arquitectura del administrador

El administrador Reproductor de Windows Media descarga usa la tecnología COM. La funcionalidad se convierte en un conjunto de interfaces de programación. Puede escribir código de programación que use estas interfaces mediante Microsoft JScript o C++.

Los lenguajes de scripting usan el concepto de objetos para dividir la funcionalidad de programación. El **modelo de objetos DownloadManager** usa varios objetos para dividir los métodos y propiedades en una organización lógica que agrupa funciones relacionadas semánticamente. Las secciones siguientes contienen información sobre los objetos del Administrador de descarga.



| Sección                                                                     | Descripción                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Acerca del objeto DownloadManager](#about-the-downloadmanager-object)       | El **objeto DownloadManager** representa el objeto raíz del Reproductor de Windows Media Download Manager. |
| [Acerca del objeto DownloadCollection](#about-the-downloadcollection-object) | El **objeto DownloadCollection** representa una colección de elementos de descarga.                             |
| [Acerca del objeto DownloadItem](#about-the-downloaditem-object)             | El **objeto DownloadItem** representa una solicitud de descarga individual.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Acerca del objeto DownloadManager

**DownloadManager** es el objeto raíz del administrador Reproductor de Windows Media descarga. Se accede a todos los demás objetos a través de este objeto . Para obtener acceso al **objeto DownloadManager,** use la siguiente sintaxis JScript datos:


```C++
var DownloadManager = external.DownloadManager;
```



Esto crea una instancia del **objeto DownloadManager,** que se puede usar para recuperar los objetos secundarios. Por ejemplo, la sintaxis siguiente recupera el primer elemento de la colección de descarga que tiene el número de identificador 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Acerca del objeto DownloadCollection

El **objeto DownloadCollection** representa una colección de archivos que se descargarán. Puede usar este objeto para determinar cuántas descargas hay en la colección, quitar elementos de la colección, recuperar un elemento de descarga específico e iniciar una nueva descarga. Al iniciar una nueva descarga, se agrega automáticamente la descarga a la colección.

## <a name="about-the-downloaditem-object"></a>Acerca del objeto DownloadItem

El **objeto DownloadItem** representa una descarga individual. Los elementos de descarga siempre existen como parte de una colección de descarga. Use este objeto para recuperar información sobre el elemento de descarga y para pausar, reanudar o cancelar la descarga en curso.

Cuando se cancela una descarga, el elemento de descarga permanece en su colección de descarga. En este caso, **downloadCollection**. **downloadState** recupera un valor de 4, lo que significa que se canceló.

Puede usar **downloadItem**. **progreso** para informar al usuario sobre la cantidad del archivo que se ha transferido o cuánto queda por descargar. Puede usar este valor para calcular también el tiempo restante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrador de descarga**](download-manager.md)
</dt> </dl>

 

 




