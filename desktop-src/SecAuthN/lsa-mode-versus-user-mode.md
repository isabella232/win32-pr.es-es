---
description: Cuando un paquete de seguridad SSP/AP funciona como un paquete de autenticación, se carga en el espacio de procesos de la autoridad de seguridad local (LSA) y se dice que está en modo LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modo LSA frente al modo usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083154"
---
# <a name="lsa-mode-vs-user-mode"></a>Modo LSA frente al modo usuario

Cuando un [*paquete de seguridad*](../secgloss/s-gly.md) SSP/AP funciona como un [*paquete de autenticación*](../secgloss/a-gly.md), se carga en el espacio de procesos de la autoridad de [*seguridad local*](../secgloss/l-gly.md) (LSA) y se dice que está en modo LSA. Las aplicaciones de inicio de sesión acceden a la funcionalidad del paquete de autenticación mediante las [funciones de inicio de sesión](authentication-functions.md) Los desarrolladores pueden usar funciones de compatibilidad con LSA disponibles únicamente para los paquetes de seguridad de modo LSA para implementar paquetes de autenticación más sofisticados que los admitidos anteriormente.

Cuando un [*paquete de seguridad*](../secgloss/s-gly.md) proporciona servicios de seguridad a una aplicación cliente/servidor, se carga en los procesos de cliente y servidor y se dice que está en modo de usuario. Las aplicaciones cliente/servidor obtienen acceso a los servicios de soporte técnico de seguridad del paquete de seguridad mediante la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) de Microsoft.

La compatibilidad de LSA con SSP/APs incluye funciones que las instancias del modo de usuario y el modo LSA de un paquete de seguridad pueden usar para comunicarse. Además, la instancia de modo de usuario de un paquete de seguridad puede delegar las solicitudes seleccionadas de información en la instancia de modo LSA del paquete.

Para obtener más información sobre cómo se inicializan los paquetes de seguridad para cada modo, consulte [inicialización en modo LSA](lsa-mode-initialization.md) y [inicialización en modo usuario](user-mode-initialization.md).

 

 
