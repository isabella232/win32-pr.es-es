---
title: La base de datos del servicio de nombres RPC
description: Un servicio de nombres es un servicio que asigna nombres a objetos y normalmente mantiene los pares (nombre, objeto) en una base de datos.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Llamada a procedimiento remoto RPC, descrita, nombre de base de datos de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361888"
---
# <a name="the-rpc-name-service-database"></a>La base de datos del servicio de nombres RPC

Un servicio de nombres es un servicio que asigna nombres a objetos y normalmente mantiene los pares (nombre, objeto) en una base de datos. Por lo general, el nombre es un nombre lógico que es fácil de recordar y usar para los usuarios. Por ejemplo, un servicio de nombres permitiría a un usuario usar el nombre lógico "printer". El servicio de nombres asigna este nombre al nombre específico de la red que usa el servidor de impresión.

Para usar una explicación simplificada, el servicio de nombres RPC asigna un nombre a un identificador de enlace y mantiene las asignaciones (nombre, identificador de enlace) en la base de datos del servicio de nombres RPC. El servicio de nombres RPC permite a las aplicaciones cliente usar un nombre lógico en lugar de una secuencia de protocolo y una dirección de red específicas. El uso del nombre lógico facilita a los administradores de red la instalación y configuración de la aplicación distribuida.

Una entrada de base de datos del servicio de nombres RPC tiene uno de los atributos siguientes: **servidor,** **grupo** o **perfil.** En la implementación de Microsoft, las entradas solo pueden tener un atributo, por lo que estas entradas también se conocen como entradas de servidor, entradas de grupo y entradas de perfil.

La entrada del servidor consta de UUID de interfaz, UUD de objeto (necesarios cuando el servidor implementa varios puntos de entrada), dirección de red, secuencia de protocolo y cualquier información de punto de conexión asociada a puntos de conexión conocidos. Cuando se usa un punto de conexión dinámico, la información del punto de conexión se mantiene en la base de datos del mapa de puntos de conexión en lugar de en la base de datos del servicio de nombres y el punto de conexión se resuelve como cualquier otro punto de conexión dinámico. Las entradas del servidor se administran mediante funciones que comienzan con el prefijo "RpcNsBinding".

La entrada de grupo puede contener entradas de servidor u otras entradas de grupo. Las entradas de grupo se administran mediante funciones que comienzan con el prefijo "RpcNsGroup".

La entrada de perfil puede contener entradas de perfil, grupo o servidor. Las entradas de perfil se administran mediante las funciones que comienzan con el prefijo "RpcNsProfile".

En esta sección se presenta información general de la base de datos del servicio de nombres en los temas siguientes:

-   [Directrices de aplicación de servicio de nombres](name-service-application-guidelines.md)
-   [Información general de la entrada del servicio name](an-overview-of-the-name-service-entry.md)
-   [Criterios para las entradas de servicio de nombre](criteria-for-name-service-entries.md)
-   [Limpieza de entrada de servicio de nombre](name-service-entry-cleanup.md)
-   [¿Qué ocurre durante una consulta?](what-happens-during-a-query.md)
-   [Uso del localizador de Microsoft](using-microsoft-locator.md)
-   [Uso de Servicio de directorio de celdas (CDS)](using-the-cell-directory-service-cds-.md)
-   [Sintaxis de nombre](name-syntax.md)

 

 




