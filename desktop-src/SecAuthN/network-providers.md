---
description: Un proveedor de red es un archivo DLL que admite un protocolo de red específico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173421"
---
# <a name="network-providers"></a>Proveedores de red

Un proveedor de red es un archivo DLL que admite un protocolo de red específico. También implementa la [API del proveedor de red](network-provider-api.md). Esto le permite interactuar con el sistema operativo Windows para recibir solicitudes de red estándar, como solicitudes de conexión o de desconexión. Para controlar estas solicitudes, el proveedor de red llama a la API específica de la red que es adecuada para el protocolo de red que admite el proveedor de red. En otras palabras, el proveedor de red encapsula la funcionalidad específica de la red en un archivo DLL, que expone una interfaz estándar a Windows.

Con los proveedores de red, Windows admite muchos tipos diferentes de protocolos de red sin tener que conocer los detalles específicos de la red de cada red. Esto es esencial porque los nuevos protocolos de red se desarrollan continuamente. Con los proveedores de red, la compatibilidad con un nuevo protocolo simplemente requiere la creación e instalación de un nuevo proveedor de red.

Para obtener información sobre las funciones y estructuras del proveedor de red, consulte los temas siguientes:

-   [Funciones del proveedor de red](authentication-functions.md)
-   [Estructuras de proveedor de red](authentication-structures.md)

 

 



