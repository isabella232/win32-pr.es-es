---
title: Publicación con puntos de conexión de servicio
description: El Active Directory define una clase de objeto serviceConnectionPoint (SCP) para facilitar que un servicio publique datos específicos del servicio en el directorio.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publicación con puntos de conexión de servicio ad
- puntos de conexión de servicio AD
- puntos de conexión de servicio AD, publicación con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c0a0e1f488ecdb50c14eb04788470b6bc25a0a3442457f1c57ced4b13efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184949"
---
# <a name="publishing-with-service-connection-points"></a>Publicación con puntos de conexión de servicio

El Active Directory esquema define una clase de objeto **serviceConnectionPoint** (SCP) para facilitar que un servicio publique datos específicos del servicio en el directorio. Los clientes del servicio usan los datos de un SCP para buscar, conectarse y autenticar una instancia del servicio.

En esta sección se proporciona información general sobre los puntos de conexión de servicio y ejemplos de código que muestran cómo una aplicación cliente/servicio usa SCP.

En el ejemplo de código se siguen estos pasos para implementar la publicación del servicio con SCP.

Para obtener más información y un ejemplo de código que realiza estos pasos, vea [Creación de un punto de conexión de servicio.](creating-a-service-connection-point.md)

**Para crear SCP en el directorio durante la instalación del servicio**

1.  Enlace al objeto de equipo para el equipo host en el que está instalada la instancia de servicio.
2.  Cree un objeto SCP como elemento secundario del objeto de equipo, especificando los valores iniciales de los atributos del SCP.
3.  Establezca entradas de control de acceso (ACE) en el descriptor de seguridad del objeto SCP para permitir que el servicio modifique las propiedades de SCP en tiempo de ejecución.
4.  Almacenar en **caché el objectGUID** del SCP en el Registro en el equipo host del servicio.

Para obtener más información y un ejemplo de código que realiza estos pasos, vea [Actualizar un punto de conexión de servicio.](updating-a-service-connection-point.md)

**Para actualizar los atributos de SCP al iniciar el servicio**

1.  Recupere el **objectGUID** del registro y úselo para enlazarlo al SCP.
2.  Recupere atributos, como **serviceDNSName y** **serviceBindingInformation,** del SCP. Compare estos valores con los valores actuales y actualice el SCP si es necesario.

Para obtener más información y un ejemplo de código que realiza estos pasos, vea [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).

**Para buscar y usar un SCP mediante una aplicación cliente**

1.  Enlace al catálogo global y busque objetos con un atributo **keywords** que coincida con el GUID del producto del servicio. Cada objeto encontrado es una instancia del servicio. Seleccione una instancia y recupere el nombre distintivo del SCP.
2.  Use el nombre completo para establecer un enlace al SCP.
3.  Recupere los valores de varios atributos del SCP, como **serviceDNSName** y **serviceBindingInformation.** Use estos valores para conectarse a la instancia de servicio y autenticarla.

Para obtener más información sobre qué roles pueden crear y actualizar un SCP, vea [Security Issues for Service Publication](security-issues-for-service-publication.md).

Para obtener más información sobre dónde crear un SCP, vea [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).

Para obtener más información sobre el tipo de datos que se almacenarán en un SCP, vea [Propiedades del punto de conexión de servicio](service-connection-point-properties.md).

Para obtener más información sobre cómo un instalador de servicio y el servicio funcionan juntos para mantener los datos actuales en un SCP, vea Crear y mantener un punto de conexión [de servicio](creating-and-maintaining-a-service-connection-point.md).

 

 




