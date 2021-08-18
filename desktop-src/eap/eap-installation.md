---
title: Instalación de EAP
description: Los proveedores implementan EAP, también conocidos como protocolos de autenticación, en bibliotecas de vínculos dinámicos (DLL).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a790f4282ef2658bacdd7f25be647234c3cf32d62ca80e8ce2745da3f4f738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984455"
---
# <a name="eap-installation"></a>Instalación de EAP

Los proveedores implementan EAP, también conocidos como protocolos de autenticación, en bibliotecas de vínculos dinámicos (DLL). Un archivo DLL para el protocolo de autenticación debe residir en los equipos cliente y servidor. Por motivos de simplicidad, los archivos DLL de cliente y servidor pueden ser idénticos; sin embargo, esto no es un requisito. Además, tenga en cuenta que el mismo archivo DLL puede admitir más de un protocolo de autenticación.

El proveedor debe proporcionar software de instalación para instalar y quitar el archivo DLL. El software de instalación también debe crear las claves y los valores adecuados para el protocolo de autenticación en el registro del sistema y quitarlas tras la desinstalación.

La instalación de cada archivo DLL de EAP debe crear la siguiente clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

En la ruta de acceso anterior, **&lt; eaptypeid &gt;** es el identificador del protocolo de autenticación. El proveedor debe obtener este identificador de internet Assigned Numbers Authority (IANA).

Para obtener más información y una descripción de los valores admitidos para esta clave, vea [Valores del Registro del protocolo de autenticación](authentication-protocol-registry-values.md).

 

 




