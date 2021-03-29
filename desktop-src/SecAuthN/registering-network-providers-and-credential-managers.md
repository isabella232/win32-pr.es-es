---
description: Una vez creado el proveedor de red o el administrador de credenciales, debe registrarlo en el sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registro de proveedores de red y administradores de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277143"
---
# <a name="registering-network-providers-and-credential-managers"></a>Registro de proveedores de red y administradores de credenciales

Una vez creado el proveedor de red o el administrador de credenciales, debe registrarlo en el sistema. Esto es necesario para que el MPR sepa qué proveedores de red están instalados. Cuando se inicia el MPR, comprueba el registro y carga los proveedores de red o administradores de credenciales que encuentra.

Dado que los proveedores de red y los administradores de credenciales están relacionados, se registran en las mismas subclaves del registro. De hecho, las dll de proveedor de red también pueden ser administradores de credenciales.

Para obtener información detallada acerca de las claves del registro que debe crear para el proveedor de red o el administrador de credenciales, consulte [claves del registro de autenticación](authentication-registry-keys.md).

 

 



