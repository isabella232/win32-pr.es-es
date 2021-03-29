---
title: Controladores de objetos
description: Controladores de objetos
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903224"
---
# <a name="object-handlers"></a>Controladores de objetos

Si una aplicación de servidor OLE es un servidor local, lo que significa que se ejecuta en su propio espacio de proceso, la comunicación entre el contenedor y el servidor debe realizarse a través de los límites del proceso. Dado que este proceso es costoso, OLE se basa en un objeto suplente cargado en el espacio de proceso del contenedor para que actúe en nombre de una aplicación de servidor local. Este objeto suplente, conocido como *controlador de objetos*, solicita a los servicios las solicitudes que no requieren la atención de la aplicación de servidor, como las solicitudes de dibujo. Cuando un contenedor solicita algo que el controlador de objetos no puede proporcionar, el controlador se comunica con la aplicación de servidor mediante el mecanismo de comunicación fuera de proceso de COM.

Un controlador de objetos es único para una clase de objeto. Cuando se crea una instancia de un controlador para una clase, no se puede utilizar para otro. Cuando se usa para un documento compuesto, el controlador de objetos implementa las estructuras de datos del contenedor cuando se tiene acceso remoto a los objetos de una clase determinada.

OLE proporciona un controlador de objetos predeterminado que pueden usar las aplicaciones de servidor locales. En el caso de las aplicaciones que requieren comportamientos especiales, los desarrolladores pueden implementar un controlador personalizado que reemplace el controlador predeterminado o lo use para proporcionar determinados comportamientos predeterminados.

Un controlador de objetos es un archivo DLL que contiene varios componentes que interactúan. Estos componentes incluyen piezas de comunicación remota para administrar la comunicación entre el controlador y su aplicación de servidor, una memoria caché para almacenar los datos de un objeto, junto con información sobre cómo deben aplicarse formato y mostrar los datos, y un objeto de control que coordina las actividades de los demás componentes del archivo DLL. Además, si un objeto es un vínculo, el archivo DLL también incluye un componente de vinculación, o un *objeto vinculado*, que realiza un seguimiento del nombre y la ubicación del origen del vínculo.

La *memoria caché* contiene datos e información de presentación suficientes para que el controlador muestre un objeto cargado pero no en ejecución en su contenedor. OLE proporciona una implementación de la memoria caché utilizada por el controlador de objetos predeterminado de OLE y el objeto de vínculo. La memoria caché almacena los datos en formatos necesarios para que el controlador de objetos satisfaga las solicitudes de dibujo del contenedor. Cuando los datos de un objeto cambian, el objeto envía una notificación a la memoria caché para que se pueda producir una actualización. Para obtener más información sobre la memoria caché, vea [ver el almacenamiento en caché](view-caching.md).

Para obtener más información, consulte el siguiente tema:

-   [Controlador predeterminado y controladores personalizados](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




