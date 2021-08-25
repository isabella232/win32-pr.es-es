---
title: Consideraciones de diseño del servidor de estado
description: En función del diseño, es posible que necesite un servidor para realizar el seguimiento de los usuarios que han iniciado sesión actualmente en la red.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39fa2460fbad5ffedd4a517da588cc0c951f734926c1219d750e28f71734c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889485"
---
# <a name="state-server-design-considerations"></a>Consideraciones de diseño del servidor de estado

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

En función del diseño, es posible que necesite un servidor para realizar el seguimiento de los usuarios que han iniciado sesión actualmente en la red. El principal desafío con el servidor de estado es mantener la información de la base de datos del servidor de estado sincronizada con quién ha iniciado sesión realmente. Si la información del servidor de estado no está sincronizada, los usuarios pueden tener correctamente varias sesiones cuando no están autorizados para hacerlo. Además, los usuarios que no tienen varias sesiones podrían ser penalizados involuntariamente.

Se debe tener en cuenta lo siguiente al implementar el servidor de estado:

-   El servidor de estado debe tomar la decisión en línea en unos segundos. Por esta razón, el servidor de estado requiere una infraestructura escalable que pueda admitir muchas actualizaciones y consultas por segundo. Las bases de datos relacionales no son adecuadas para consultas de gran tamaño con actualizaciones simultáneas. Las bases de datos relacionales se han creado principalmente para mantener la coherencia de los datos y proporcionar una vista coherente de los datos a todos los consumidores. No se han creado para actualizaciones rápidas.
-   La coherencia transaccional en las actualizaciones entre varios objetos no es importante. Esto se debe a que el servidor de estado puede tolerar una pequeña ventana de oportunidad. Sin embargo, la coherencia transaccional de una sola actualización es importante para reducir las posibilidades de dejar el servidor de estado en un estado incoherente si uno de los servidores RADIUS se apaga en medio de la actualización.
-   La persistencia (guardar el estado de la red en un almacenamiento persistente) no es importante porque la información persistente se desa sincronizará rápidamente con el estado real de la red.
-   Si se admiten ISDN u otras formas de vínculo múltiple en la red, el servidor de estado debe ser capaz de controlar escenarios que usan estas características.

Un posible diseño es implementar un archivo DLL de extensión de autenticación y un archivo DLL de extensión de autorización. Cada uno de estos archivos DLL puede comunicarse a través de la red con una base de datos. El archivo DLL de la extensión de autorización puede actualizar la base de datos con información sobre quién ha iniciado sesión actualmente en la red. El archivo DLL de extensión de autenticación puede consultar esta información en la base de datos para decidir si se acepta o rechaza la solicitud de autenticación de un usuario determinado. Si el usuario ya ha iniciado sesión, se rechaza la solicitud.

La ventaja de que el archivo DLL de la extensión de autorización actualice la base de datos de servidor de estado es que el archivo DLL de la extensión de autorización tiene acceso a más información sobre el usuario autenticado. El archivo DLL de la extensión de autorización tiene acceso a todos los atributos de autorización del mecanismo de autorización de NPS. Por ejemplo, algunos usuarios pueden tener autorizaciones que les permitan tener varias sesiones. El servidor de estado debe tratar a estos usuarios como un caso especial.

 

 




