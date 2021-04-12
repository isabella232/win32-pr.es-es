---
description: Un proveedor de red es un archivo DLL que admite un protocolo de red específico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Proveedores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278124"
---
# <a name="network-providers"></a>Proveedores de red

Un proveedor de red es un archivo DLL que admite un protocolo de red específico. También implementa la API del [proveedor de red](network-provider-api.md). Esto le permite interactuar con el sistema operativo Windows para recibir solicitudes de red estándar, como solicitudes de conexión o desconexión. Para controlar estas solicitudes, el proveedor de red llama entonces a la API específica de la red que sea adecuada para el protocolo de red que admite el proveedor de red. En otras palabras, el proveedor de red ajusta la funcionalidad específica de la red en un archivo DLL, que expone una interfaz estándar a Windows.

Mediante el uso de proveedores de red, Windows puede admitir muchos tipos diferentes de protocolos de red sin tener que conocer los detalles específicos de la red de cada red. Esto es esencial porque los nuevos protocolos de red se están desarrollando todo el tiempo. Con los proveedores de red, la compatibilidad con un nuevo protocolo requiere la creación e instalación de un nuevo proveedor de red.

Para obtener información sobre las funciones y estructuras de proveedor de red, vea los temas siguientes:

-   [Funciones de proveedor de red](authentication-functions.md)
-   [Estructuras de proveedor de red](authentication-structures.md)

 

 



