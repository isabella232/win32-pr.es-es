---
title: Modificar el valor predeterminado de redirección del dispositivo
description: Dado que Escritorio remoto servidores de puerta de enlace intentan exigir directivas de redirección de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903548"
---
# <a name="modify-device-redirection-default"></a>Modificar el valor predeterminado de redirección del dispositivo

Dado que Escritorio remoto servidores de puerta de enlace intentan exigir directivas de redirección de dispositivos seguras antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.

En Windows Server 2008 R2 y versiones posteriores, los servidores de puerta de enlace de Escritorio remoto de forma predeterminada intentarán aplicar directivas seguras de redireccionamiento de dispositivos antes de pasar la conexión de cliente a un servidor host de sesión Escritorio remoto. Sin embargo, esta característica no es compatible con algunos servidores. Por ejemplo, esto no se admite para las conexiones a las sesiones de la consola de Hyper-V y es posible que sea necesario deshabilitar el valor predeterminado para admitir la autenticación federada. En estos casos, esta característica puede deshabilitarse mediante la creación de la siguiente clave del registro para permitir que las conexiones pasen.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server Gateway \\ preRDPDisableRegKey**

Cuando exista esta clave, la puerta de enlace de Escritorio remoto no aplicará la redirección de dispositivos.

 

 




