---
title: Clases y servidores
description: Clases y servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421464"
---
# <a name="classes-and-servers"></a>Clases y servidores

COM utiliza **\_ las clases HKEY \_ raíz** para la configuración de todo el equipo, pero también permite la configuración por usuario de CLSID para una mayor seguridad y flexibilidad. COM consulta primero **\_ \_ \\ \\ las clases de software de usuario actuales de HKEY** antes de buscar en **HKEY \_ classes \_ root**. COM mantiene la información de todo el equipo relacionada con los CLSID en **\_ las clases HKEY \_ raíz \\ CLSID** y mantiene la información de clase por usuario en **HKEY \_ Current \_ User \\ \\ classes \\ CLSID**.

Los servidores COM admiten el registro automático. Para un servidor en proceso, esto significa que el archivo DLL debe exportar las siguientes funciones:

-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Debe exportar explícitamente estas funciones mediante un archivo de definición de módulo, modificadores del enlazador o directivas de compilador. El almacén de clases utiliza estas funciones para configurar el registro local después de descargar el archivo en el equipo cliente. Además del almacén de clases, otras funciones también se usan en otros entornos para instalar servidores en equipos host.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 