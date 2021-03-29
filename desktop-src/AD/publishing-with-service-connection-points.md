---
title: Publicar con puntos de conexión de servicio
description: El esquema de Active Directory define una clase de objeto serviceConnectionPoint (SCP) para facilitar a un servicio la publicación de datos específicos del servicio en el directorio.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publicación con puntos de conexión de servicio AD
- puntos de conexión de servicio AD
- puntos de conexión de servicio AD, publicación con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773111"
---
# <a name="publishing-with-service-connection-points"></a>Publicar con puntos de conexión de servicio

El esquema de Active Directory define una clase de objeto **serviceConnectionPoint** (SCP) para facilitar a un servicio la publicación de datos específicos del servicio en el directorio. Los clientes del servicio usan los datos de un SCP para buscar, conectarse y autenticar una instancia de su servicio.

En esta sección se proporciona información general sobre los puntos de conexión de servicio y ejemplos de código que muestran cómo una aplicación de cliente o servicio utiliza los SCP.

En el ejemplo de código se siguen estos pasos para implementar la publicación de servicio con SCP.

Para obtener más información y un ejemplo de código que realice estos pasos, consulte [crear un punto de conexión de servicio](creating-a-service-connection-point.md).

**Para crear SCP en el directorio en la instalación del servicio**

1.  Enlazar al objeto de equipo para el equipo host en el que está instalada la instancia de servicio.
2.  Cree un objeto SCP como elemento secundario del objeto Computer y especifique los valores iniciales de los atributos del SCP.
3.  Establezca entradas de control de acceso (ACE) en el descriptor de seguridad del objeto SCP para permitir que el servicio modifique las propiedades de SCP en tiempo de ejecución.
4.  Almacene en caché el **objectGUID** del SCP en el registro en el equipo host del servicio.

Para obtener más información y un ejemplo de código que realice estos pasos, vea [actualizar un punto de conexión de servicio](updating-a-service-connection-point.md).

**Para actualizar los atributos de SCP en el inicio del servicio**

1.  Recupere el **objectGUID** del registro y úselo para enlazar con el SCP.
2.  Recupere los atributos, como **serviceDNSName** y **SERVICEBINDINGINFORMATION**, del SCP. Compare estos valores con los valores actuales y actualice el SCP si es necesario.

Para obtener más información y un ejemplo de código que realice estos pasos, vea [cómo los clientes buscan y usan un punto de conexión de servicio](how-clients-find-and-use-a-service-connection-point.md).

**Para buscar y usar un SCP por parte de una aplicación cliente**

1.  Enlazar con el catálogo global y buscar objetos con un atributo **Keywords** que coincida con el GUID del producto del servicio. Cada objeto encontrado es una instancia del servicio. Seleccione una instancia y recupere el nombre distintivo del SCP.
2.  Use el nombre completo para establecer un enlace al SCP.
3.  Recupere los valores de varios atributos del SCP, como **serviceDNSName** y **serviceBindingInformation**. Use estos valores para conectarse a la instancia de servicio y autenticarla.

Para obtener más información sobre los roles que pueden crear y actualizar un SCP, consulte [problemas de seguridad de la publicación de servicio](security-issues-for-service-publication.md).

Para obtener más información acerca de dónde crear un SCP, consulte [dónde crear un punto de conexión de servicio](where-to-create-a-service-connection-point.md).

Para obtener más información sobre el tipo de datos que se almacenan en un SCP, consulte [propiedades de punto de conexión de servicio](service-connection-point-properties.md).

Para obtener más información sobre cómo un instalador de servicio y el servicio trabajan juntos para mantener los datos actuales en un SCP, vea [crear y mantener un punto de conexión de servicio](creating-and-maintaining-a-service-connection-point.md).

 

 




