---
description: Después de crear el proveedor de red o el administrador de credenciales, debe registrarlo en el sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registro de proveedores de red y administradores de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069125"
---
# <a name="registering-network-providers-and-credential-managers"></a>Registro de proveedores de red y administradores de credenciales

Después de crear el proveedor de red o el administrador de credenciales, debe registrarlo en el sistema. Esto es necesario para que MPR sepa qué proveedores de red están instalados. Cuando se inicia MPR, comprueba el registro y carga los proveedores de red o administradores de credenciales que encuentre.

Dado que los proveedores de red y los administradores de credenciales están relacionados, se registran en las mismas subclaves del registro. De hecho, los archivos DLL del proveedor de red también pueden ser administradores de credenciales.

Para obtener información detallada sobre las claves del Registro que debe crear para el proveedor de red o el administrador de credenciales, vea [Claves del Registro de autenticación](authentication-registry-keys.md).

 

 



