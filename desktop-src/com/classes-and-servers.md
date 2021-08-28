---
title: Clases y servidores
description: Clases y servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b87ce6b52e73f8ac4e465202b787a2c65dc563f3d7c0678ef82b91601351d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993805"
---
# <a name="classes-and-servers"></a>Clases y servidores

COM usa **HKEY \_ CLASSES ROOT \_ para** la configuración de todo el equipo, pero también permite la configuración por usuario de CLSIDS para mayor seguridad y flexibilidad. COM consulta primero las clases **de software HKEY \_ CURRENT USER \_ \\ \\ antes** de buscar en **HKEY CLASSES \_ \_ ROOT**. COM mantiene la información de todo el equipo relacionada con los CLSID en **HKEY \_ CLASSES ROOT \_ \\ CLSID** y mantiene la información de clase por usuario en **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ CLSID**.

Los servidores COM admiten el registro propio. Para un servidor en proceso, esto significa que el archivo DLL debe exportar las funciones siguientes:

-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Debe exportar explícitamente estas funciones mediante un archivo de definición de módulo, modificadores de vinculador o directivas del compilador. El almacén de clases usa estas funciones para configurar el registro local después de descargar el archivo en el equipo cliente. Además del almacén de clases, otros entornos también usan estas funciones para instalar servidores en equipos host.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 