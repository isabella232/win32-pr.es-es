---
title: La base de datos del servicio de nombres RPC
description: Un servicio de nombres es un servicio que asigna nombres a objetos y normalmente mantiene los pares (nombre, objeto) en una base de datos.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Llamada a procedimiento remoto RPC, descripción, nombre base de datos de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486874"
---
# <a name="the-rpc-name-service-database"></a>La base de datos del servicio de nombres RPC

Un servicio de nombres es un servicio que asigna nombres a objetos y normalmente mantiene los pares (nombre, objeto) en una base de datos. Por lo general, el nombre es un nombre lógico que es fácil de recordar para los usuarios. Por ejemplo, un servicio de nombres permitiría que un usuario utilizara el nombre lógico "laserprinter". El servicio de nombres asigna este nombre al nombre específico de la red que usa el servidor de impresión.

Para usar una explicación simplificada, el servicio de nombres RPC asigna un nombre a un identificador de enlace y mantiene las asignaciones (nombre, identificador de enlace) en la base de datos del servicio de nombres de RPC. El servicio de nombres RPC permite a las aplicaciones cliente utilizar un nombre lógico en lugar de una secuencia de protocolo y una dirección de red específicas. El uso del nombre lógico facilita a los administradores de red la instalación y configuración de la aplicación distribuida.

Una entrada de base de datos del servicio de nombres RPC tiene uno de los siguientes atributos: **servidor**, **Grupo** o **perfil**. En la implementación de Microsoft, las entradas solo pueden tener un atributo, por lo que estas entradas también se conocen como entradas de servidor, entradas de grupo y entradas de perfil.

La entrada del servidor consiste en la interfaz UUID, el objeto UUID (necesario cuando el servidor implementa puntos de entrada múltiples), la dirección de red, la secuencia de protocolo y cualquier información de punto de conexión asociada con puntos de conexión conocidos. Cuando se usa un punto de conexión dinámico, la información del punto de conexión se mantiene en la base de datos de asignación de extremos en lugar de en la base de datos del servicio de nombres y el punto de conexión se resuelve como cualquier otro punto de conexión dinámico. Las entradas del servidor se administran mediante funciones que comienzan con el prefijo "RpcNsBinding".

La entrada de grupo puede contener entradas de servidor u otras entradas de grupo. Las entradas de grupo se administran mediante funciones que comienzan con el prefijo "RpcNsGroup".

La entrada de perfil puede contener entradas de perfil, de grupo o de servidor. Las funciones que empiezan por el prefijo "RpcNsProfile" administran las entradas de perfil.

En esta sección se presenta una introducción a la base de datos del servicio de nombres en los temas siguientes:

-   [Instrucciones de aplicación de servicio de nombres](name-service-application-guidelines.md)
-   [Información general de la entrada del servicio de nombres](an-overview-of-the-name-service-entry.md)
-   [Criterios para las entradas del servicio de nombres](criteria-for-name-service-entries.md)
-   [Limpieza de entradas del servicio de nombres](name-service-entry-cleanup.md)
-   [Lo que sucede durante una consulta](what-happens-during-a-query.md)
-   [Uso del localizador de Microsoft](using-microsoft-locator.md)
-   [Uso del Servicio de directorio de celdas (CDS)](using-the-cell-directory-service-cds-.md)
-   [Sintaxis de nombre](name-syntax.md)

 

 




