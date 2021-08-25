---
title: Controladores de objetos
description: Controladores de objetos
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85221456d637e0d9e982aad253c06d34618018a3648a31a7bd21e8c1465fa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992325"
---
# <a name="object-handlers"></a>Controladores de objetos

Si una aplicación de servidor OLE es un servidor local, lo que significa que se ejecuta en su propio espacio de proceso, la comunicación entre el contenedor y el servidor debe producirse a través de los límites del proceso. Dado que este proceso es costoso, OLE se basa en un objeto suplente cargado en el espacio de proceso del contenedor para actuar en nombre de una aplicación de servidor local. Este objeto suplente, conocido como controlador de objetos *,* proporciona solicitudes de contenedor que no requieren la atención de la aplicación de servidor, como las solicitudes de dibujo. Cuando un contenedor solicita algo que el controlador de objetos no puede proporcionar, el controlador se comunica con la aplicación de servidor mediante el mecanismo de comunicación fuera de proceso de COM.

Un controlador de objetos es único para una clase de objeto. Cuando se crea una instancia de un controlador para una clase, no se puede usar para otra. Cuando se usa para un documento compuesto, el controlador de objetos implementa las estructuras de datos del lado contenedor cuando se accede a los objetos de una clase determinada de forma remota.

OLE proporciona un controlador de objetos predeterminado que las aplicaciones de servidor local pueden usar. En el caso de las aplicaciones que requieren comportamientos especiales, los desarrolladores pueden implementar un controlador personalizado que reemplace el controlador predeterminado o lo use para proporcionar determinados comportamientos predeterminados.

Un controlador de objetos es un archivo DLL que contiene varios componentes que interactúan. Estos componentes incluyen partes de comunicación remota para administrar la comunicación entre el controlador y su aplicación de servidor, una memoria caché para almacenar los datos de un objeto, junto con información sobre cómo se deben dar formato y mostrar esos datos, y un objeto de control que coordina las actividades de los demás componentes del archivo DLL. Además, si un objeto es un vínculo, el archivo DLL también incluye un componente de vinculación o un objeto vinculado *,* que realiza un seguimiento del nombre y la ubicación del origen del vínculo.

La *memoria caché* contiene datos e información de presentación suficiente para que el controlador muestre un objeto cargado, pero no en ejecución, en su contenedor. OLE proporciona una implementación de la memoria caché utilizada por el controlador de objetos predeterminado de OLE y el objeto de vínculo. La memoria caché almacena los datos en formatos necesarios para que el controlador de objetos satisfaga las solicitudes de dibujo del contenedor. Cuando cambian los datos de un objeto, el objeto envía una notificación a la memoria caché para que se pueda producir una actualización. Para obtener más información sobre la memoria caché, vea [Ver almacenamiento en caché.](view-caching.md)

Para obtener más información, consulte el siguiente tema:

-   [Controlador predeterminado y controladores personalizados](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




