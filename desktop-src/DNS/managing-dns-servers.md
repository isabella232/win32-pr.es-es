---
title: Administración de servidores DNS
description: Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777964"
---
# <a name="managing-dns-servers"></a>Administración de servidores DNS

Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS. Los servidores DNS contienen archivos, denominados *archivos de zona*, que les permiten resolver nombres en direcciones IP (o viceversa). Cuando se consulta, un servidor DNS responde de una de estas tres maneras:

-   El servidor devuelve la información de resolución de nombres o resolución de IP solicitada.
-   El servidor devuelve un puntero a otro servidor DNS que puede atender la solicitud.
-   El servidor indica que no tiene la información solicitada.

Los servidores DNS podrían, durante el transcurso de la preparación de la devolución de la información de resolución solicitada, consultar otros servidores DNS. Pero más allá de eso, los servidores DNS no realizan ninguna operación distinta de la mencionada en la lista anterior.

Hay tres tipos principales de servidores DNS: los servidores principales, los servidores secundarios y los servidores de almacenamiento en caché. Consulte [servidores DNS](dns-servers.md) para obtener más información acerca de estos servidores DNS.

## <a name="administration-steps"></a>Pasos de administración

El proveedor WMI de DNS permite la administración de servidores DNS desde el propio servidor o desde hosts remotos. Los pasos generales necesarios para administrar un servidor DNS con el proveedor WMI de DNS son los siguientes:

-   Conexión al proveedor WMI de DNS
-   Obtener una instancia de servidor
-   Enumerar o modificar una propiedad de servidor, o usar un método

Para ilustrar cómo implementar esos pasos de administración, se proporcionan ejemplos. Las siguientes tareas están vinculadas a sus ejemplos de scripting asociados.

-   [Detención de un servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Inicio de un servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Reinicio de un servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Agregar una dirección IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Quitar una dirección IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Enumerar las propiedades del servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Mostrar tipos de propiedades de servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Modificación de las propiedades del servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




