---
title: Clases y servidores
description: Clases y servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369676"
---
# <a name="classes-and-servers"></a>Clases y servidores

COM usa **HKEY \_ CLASSES ROOT \_ para** la configuración de todo el equipo, pero también permite la configuración por usuario de CLSIDS para mayor seguridad y flexibilidad. COM consulta primero las clases **de software HKEY \_ CURRENT \_ USER \\ \\** antes de buscar en **HKEY CLASSES \_ \_ ROOT**. COM mantiene la información de todo el equipo relacionada con LOS CLID en **HKEY \_ CLASSES ROOT \_ \\ CLSID** y mantiene la información de clase por usuario en **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ CLSID**.

Los servidores COM admiten el registro propio. Para un servidor en proceso, esto significa que el archivo DLL debe exportar las siguientes funciones:

-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Debe exportar explícitamente estas funciones mediante un archivo de definición de módulo, modificadores del vinculador o directivas del compilador. El almacén de clases usa estas funciones para configurar el registro local después de descargar el archivo en el equipo cliente. Además del almacén de clases, otros entornos también usan estas funciones para instalar servidores en equipos host.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 