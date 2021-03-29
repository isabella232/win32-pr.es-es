---
title: Consideraciones sobre el diseño del servidor de estado
description: Dependiendo del diseño, puede que necesite un servidor para realizar un seguimiento de los usuarios que han iniciado sesión actualmente en la red.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0ef654f3641138075acc667d733b20c94c4840
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418940"
---
# <a name="state-server-design-considerations"></a>Consideraciones sobre el diseño del servidor de estado

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

Dependiendo del diseño, puede que necesite un servidor para realizar un seguimiento de los usuarios que han iniciado sesión actualmente en la red. El principal desafío del servidor de estado es mantener sincronizada la información de la base de datos del servidor de estado con la que ha iniciado sesión realmente. Si la información del servidor de estado no está sincronizada, es posible que los usuarios tengan varias sesiones cuando no estén autorizadas para ello. Además, los usuarios que no tienen varias sesiones podrían penalizarse accidentalmente.

Se debe tener en cuenta lo siguiente para implementar el servidor de estado:

-   El servidor de Estado debe poner en línea la decisión en unos segundos. Por esta razón, el servidor de estado requiere una infraestructura escalable que pueda admitir muchas actualizaciones y consultas por segundo. Las bases de datos relacionales no son adecuadas para consultas de gran tamaño con actualizaciones simultáneas. Las bases de datos relacionales se compilan principalmente para mantener la coherencia de los datos y proporcionar una vista coherente de los datos para todos los consumidores. No se compilan para las actualizaciones rápidas.
-   La coherencia transaccional en las actualizaciones entre varios objetos no es importante. Esto se debe a que el servidor de estado puede tolerar una pequeña ventana de oportunidad. Sin embargo, la coherencia transaccional de una sola actualización es importante para reducir las posibilidades de que el servidor de estado se quede en un estado incoherente si uno de los servidores RADIUS se apaga en medio de la actualización.
-   La persistencia (guardar el estado de la red en un almacenamiento persistente) no es importante, ya que la información persistente dejará de sincronizarse rápidamente con el estado real de la red.
-   Si se admiten ISDN (RDSI) u otras formas de multivínculo en la red, el servidor de Estado debe ser capaz de controlar los escenarios que utilizan estas características.

Un posible diseño es implementar un archivo DLL de extensión de autenticación y un archivo DLL de extensión de autorización. Cada uno de estos archivos dll puede comunicarse a través de la red con una base de datos de. El archivo DLL de la extensión de autorización puede actualizar la base de datos con información sobre quién ha iniciado sesión actualmente en la red. El archivo DLL de extensión de autenticación puede consultar la base de datos para obtener esta información y decidir si aceptar o rechazar la solicitud de autenticación de un usuario determinado. Si el usuario ya ha iniciado sesión, se rechazará la solicitud.

La ventaja de tener la DLL de extensión de autorización para actualizar la base de datos de estado es que el archivo DLL de extensión de autorización tiene acceso a más información sobre el usuario autenticado. El archivo DLL de la extensión de autorización tiene acceso a todos los atributos de autorización del mecanismo de autorización de NPS. Por ejemplo, algunos usuarios pueden tener autorizaciones que les permitan tener varias sesiones. El servidor de Estado debe tratar a estos usuarios como un caso especial.

 

 




