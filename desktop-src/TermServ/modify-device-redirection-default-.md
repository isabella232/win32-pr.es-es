---
title: Modificar el valor predeterminado de redirección de dispositivos
description: Dado que Escritorio remoto Gateway intenta aplicar directivas de redireccionamiento de dispositivos seguros antes de pasar la conexión de cliente a un servidor host de sesión de Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b74515f6bf79b42c129ec7c113729b9871d4e4bfb0101f845f91dcac0d49237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138181"
---
# <a name="modify-device-redirection-default"></a>Modificar el valor predeterminado de redirección de dispositivos

Dado que Escritorio remoto Gateway intenta aplicar directivas de redireccionamiento de dispositivos seguros antes de pasar la conexión de cliente a un servidor host de sesión de Escritorio remoto, puede que tenga que deshabilitar este valor predeterminado en algunos casos.

En Windows Server 2008 R2 y versiones posteriores, los servidores de puerta de enlace de Escritorio remoto intentarán de forma predeterminada aplicar directivas de redireccionamiento de dispositivos seguros antes de pasar la conexión de cliente a un servidor host de sesión de Escritorio remoto. Sin embargo, algunos servidores no admiten esta característica. Por ejemplo, esto no se admite para las conexiones a sesiones de consola de Hyper-V y puede ser necesario deshabilitar el valor predeterminado para admitir la autenticación federada. En estos casos, esta característica se puede deshabilitar mediante la creación de la siguiente clave del Registro para permitir que pasen las conexiones.

**HKEY \_ LOCAL MACHINE Software Microsoft Terminal Server Gateway \_ \\ \\ \\ \\ preRDPDisableRegKey**

Cuando esta clave existe, la Escritorio remoto de enlace no aplicará el redireccionamiento del dispositivo.

 

 




