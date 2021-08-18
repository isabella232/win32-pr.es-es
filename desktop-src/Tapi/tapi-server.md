---
description: El servidor TAPI (TAPISRV) es el repositorio central de datos de telefonía en un equipo de usuario.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Servidor TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19eb335ddef68f5f4cc588e34edab4931ad8be1e5e1d768e07a142989afe2291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002683"
---
# <a name="tapi-server"></a>Servidor TAPI

El servidor TAPI (TAPISRV) es el repositorio central de datos de telefonía en un equipo de usuario. Este proceso de servicio realiza un seguimiento de los recursos de telefonía locales y remotos, las aplicaciones registradas para controlar las solicitudes de telefonía asistida y las funciones asincrónicas pendientes, y también permite una interfaz coherente con proveedores de servicios de telefonía (TSP). Para obtener más información y un diagrama que ilustra la relación del servidor TAPI con otros componentes y una visión general de sus roles, vea Modelo de programación [de telefonía de Microsoft](microsoft-telephony-programming-model.md).

Para equipos que se ejecutan en sistemas operativos Windows Server 2003, Windows XP y Windows 2000, TAPISRV se ejecuta en el contexto de Svchost.exe. Para los equipos que se Windows NT, se ejecuta como un proceso de servicio independiente. Cuando una aplicación carga un archivo DLL de TAPI en su espacio de proceso y realiza una operación de inicialización, el archivo DLL establece un vínculo RPC al servidor TAPI. El servidor TAPI carga los proveedores de servicios telefónicos (TSP) en su espacio de proceso. Independientemente de cuántas aplicaciones accedan a los dispositivos de un proveedor determinado, solo existirá una instancia de un TSP determinado.

 

 



