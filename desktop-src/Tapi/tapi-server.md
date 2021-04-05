---
description: El servidor TAPI (TAPISRV) es el repositorio central de datos de telefonía en un equipo de usuario.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Servidor TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911530"
---
# <a name="tapi-server"></a>Servidor TAPI

El servidor TAPI (TAPISRV) es el repositorio central de datos de telefonía en un equipo de usuario. Este proceso de servicio realiza un seguimiento de los recursos de telefonía locales y remotos, las aplicaciones registradas para administrar las solicitudes de telefonía asistidas y las funciones asincrónicas pendientes, además de habilitar una interfaz coherente con los proveedores de servicios de telefonía (profesionales). Para obtener más información y un diagrama que muestra la relación entre el servidor TAPI y otros componentes, así como información general de sus roles, vea [modelo de programación de telefonía de Microsoft](microsoft-telephony-programming-model.md).

En el caso de los equipos que se ejecutan en sistemas operativos Windows Server 2003, Windows XP y Windows 2000, TAPISRV se ejecuta en el contexto de Svchost.exe. En el caso de los equipos que ejecutan Windows NT, se ejecuta como un proceso de servicio independiente. Cuando una aplicación carga una DLL de TAPI en su espacio de proceso y realiza una operación de inicialización, el archivo DLL establece un vínculo RPC al servidor TAPI. El servidor TAPI carga los proveedores de servicios telefónicos (profesionales) en su espacio de proceso. Independientemente del número de aplicaciones que accedan a los dispositivos de un proveedor determinado, solo existirá una instancia de un TSP determinado.

 

 



