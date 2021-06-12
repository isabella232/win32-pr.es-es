---
title: Administración de servidores DNS
description: Obtenga información sobre la administración de servidores DNS. Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010779"
---
# <a name="managing-dns-servers"></a>Administración de servidores DNS

Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS. Los servidores DNS contienen archivos, denominados *archivos de zona,* que les permiten resolver nombres en direcciones IP (o viceversa). Cuando se consulta, un servidor DNS responde de una de estas tres maneras:

-   El servidor devuelve la información de resolución de nombres o resolución IP solicitada.
-   El servidor devuelve un puntero a otro servidor DNS que puede dar servicio a la solicitud.
-   El servidor indica que no tiene la información solicitada.

Durante la preparación de la preparación para devolver la información de resolución solicitada, los servidores DNS podrían consultar otros servidores DNS. Pero más allá de eso, los servidores DNS no realizan ninguna operación que no sea la mencionada en la lista anterior.

Hay tres tipos principales de servidores DNS: servidores principales, servidores secundarios y servidores de almacenamiento en caché. Consulte [Servidores DNS para](dns-servers.md) obtener más información sobre estos servidores DNS.

## <a name="administration-steps"></a>Pasos de administración

El proveedor WMI de DNS permite la administración de servidores DNS desde el propio servidor o desde hosts remotos. Los pasos generales necesarios para administrar un servidor DNS mediante el proveedor WMI de DNS son:

-   Conexión al proveedor WMI de DNS
-   Obtención de una instancia de servidor
-   Enumerar o modificar una propiedad de servidor o usar un método

Para ilustrar cómo implementar esos pasos de administración, se proporcionan ejemplos. Las tareas siguientes están vinculadas a sus ejemplos de scripting asociados.

-   [Detención de un servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Iniciar un servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Reiniciar un servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Adición de una dirección IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Eliminación de una dirección IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Enumeración de las propiedades del servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Mostrar tipos de propiedades de servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Modificar las propiedades del servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




