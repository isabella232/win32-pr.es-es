---
description: Cuando un paquete de seguridad SSP/AP funciona como un paquete de autenticación, se carga en el espacio de proceso de la autoridad de seguridad local (LSA) y se dice que está en modo LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modo LSA frente al modo de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa965cd66f43548243c1e62329e6d9d337a2a0123344a8cb9f10915846a765f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922084"
---
# <a name="lsa-mode-vs-user-mode"></a>Modo LSA frente al modo de usuario

Cuando un paquete de [](../secgloss/s-gly.md) seguridad SSP/AP funciona como un paquete de autenticación, [](../secgloss/a-gly.md)se carga en el espacio de proceso de la autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA) y se dice que está en modo LSA. Las aplicaciones de inicio de sesión acceden a la funcionalidad del paquete de autenticación mediante las [funciones de inicio de sesión de LSA](authentication-functions.md). Los desarrolladores pueden usar las funciones de compatibilidad de LSA disponibles solo para los paquetes de seguridad en modo LSA para implementar paquetes de autenticación más sofisticados de los que se admiten anteriormente.

Cuando un [*paquete de seguridad*](../secgloss/s-gly.md) proporciona servicios de seguridad a una aplicación cliente/servidor, se carga en los procesos de cliente y servidor y se dice que está en modo de usuario. Las aplicaciones cliente/servidor acceden a los servicios de soporte técnico de seguridad del paquete de seguridad mediante la Interfaz [*del*](../secgloss/s-gly.md) proveedor de soporte técnico de seguridad (SSPI) de Microsoft.

La compatibilidad de LSA con SSP/AP incluye funciones que las instancias de modo LSA y modo de usuario de un paquete de seguridad pueden usar para comunicarse. Además, la instancia en modo de usuario de un paquete de seguridad puede delegar las solicitudes seleccionadas de información a la instancia en modo LSA del paquete.

Para obtener más información sobre cómo se inicializan los paquetes de seguridad para cada modo, vea Inicialización en modo [LSA](lsa-mode-initialization.md) e [Inicialización en modo de usuario](user-mode-initialization.md).

 

 
