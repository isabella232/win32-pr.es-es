---
title: Instalación de EAP
description: Los proveedores implementan EAPs, también conocidos como protocolos de autenticación, en bibliotecas de vínculos dinámicos (dll).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420027"
---
# <a name="eap-installation"></a>Instalación de EAP

Los proveedores implementan EAPs, también conocidos como protocolos de autenticación, en bibliotecas de vínculos dinámicos (dll). Un archivo DLL para el protocolo de autenticación debe residir en los equipos cliente y servidor. Para simplificar, los archivos dll de cliente y servidor pueden ser idénticos; sin embargo, esto no es un requisito. Además, tenga en cuenta que el mismo archivo DLL puede admitir más de un protocolo de autenticación.

El proveedor debe proporcionar el software de instalación para instalar y quitar el archivo DLL. El software de instalación también debe crear las claves y los valores adecuados para el protocolo de autenticación en el registro del sistema y quitarlos tras la desinstalación.

La instalación de cada archivo DLL de EAP debe crear la siguiente clave del registro.

**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **servicios** \\ **rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

En la ruta de acceso anterior, **&lt; eaptypeid &gt;** es el identificador del Protocolo de autenticación. El proveedor debe obtener este identificador de la autoridad de asignación de números de Internet (IANA).

Para obtener más información y una descripción de los valores admitidos para esta clave, consulte [valores del registro del Protocolo de autenticación](authentication-protocol-registry-values.md).

 

 




