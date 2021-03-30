---
title: Arquitectura de Download Manager
description: Arquitectura de Download Manager
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- arquitectura del administrador de descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774095"
---
# <a name="download-manager-architecture"></a>Arquitectura de Download Manager

El administrador de descargas de Windows Media Player usa la tecnología COM. La funcionalidad se divide en un conjunto de interfaces de programación; puede escribir código de programación que use estas interfaces mediante Microsoft JScript o C++.

Los lenguajes de scripting usan el concepto de objetos para dividir la funcionalidad de programación. El modelo de objetos **Downloadmanager** utiliza varios objetos para dividir los métodos y las propiedades en una organización lógica que agrupa las funciones relacionadas semánticamente. Las secciones siguientes contienen información sobre los objetos del administrador de descargas.



| Sección                                                                     | Descripción                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Acerca del objeto DownloadManager](#about-the-downloadmanager-object)       | El objeto **Downloadmanager** representa el objeto raíz para el administrador de descargas de Windows Media Player. |
| [Acerca del objeto DownloadCollection](#about-the-downloadcollection-object) | El objeto **DownloadCollection** representa una colección de elementos de descarga.                             |
| [Acerca del objeto DownloadItem](#about-the-downloaditem-object)             | El objeto **DownloadItem** representa una solicitud de descarga individual.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Acerca del objeto DownloadManager

**Downloadmanager** es el objeto raíz para el administrador de descargas de Windows Media Player. Se tiene acceso a todos los demás objetos a través de este objeto. Para obtener acceso al objeto **Downloadmanager** , use la siguiente sintaxis de JScript:


```C++
var DownloadManager = external.DownloadManager;
```



Esto crea una instancia del objeto **Downloadmanager** , que se puede usar para recuperar los objetos secundarios. Por ejemplo, la siguiente sintaxis recupera el primer elemento de la colección de descarga que tiene el identificador número 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Acerca del objeto DownloadCollection

El objeto **DownloadCollection** representa una colección de archivos que se van a descargar. Puede utilizar este objeto para determinar el número de descargas que hay en la colección, quitar elementos de la colección, recuperar un elemento de descarga específico e iniciar una nueva descarga. Al iniciar una nueva descarga, se agrega automáticamente la descarga a la colección.

## <a name="about-the-downloaditem-object"></a>Acerca del objeto DownloadItem

El objeto **DownloadItem** representa una descarga individual. Los elementos de descarga siempre existen como parte de una colección de descargas. Utilice este objeto para recuperar información sobre el elemento de descarga y para pausar, reanudar o cancelar la descarga en curso.

Al cancelar una descarga, el elemento de descarga permanece en su lugar en la colección de descargas. En este caso, **downloadCollection**. **downloadState** recupera un valor de 4, lo que significa que se canceló.

Puede usar **downloadItem**. **progreso** para informar al usuario sobre la cantidad del archivo que se ha transferido o la cantidad de tiempo que se va a descargar. Puede usar este valor para calcular también el tiempo restante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrador de descargas**](download-manager.md)
</dt> </dl>

 

 




