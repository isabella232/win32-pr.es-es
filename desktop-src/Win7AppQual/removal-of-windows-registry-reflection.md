---
description: Eliminación de la Windows del Registro
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Eliminación de la Windows del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9fcd31686754f9bf2d92994bec4a53b39edaf5d94b34f464e1dfdbf1179c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328984"
---
# <a name="removal-of-windows-registry-reflection"></a>Eliminación de la Windows del Registro

## <a name="platform"></a>Plataforma

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

El proceso de reflexión del Registro copia las claves y los valores del Registro entre dos vistas del Registro para mantenerlos sincronizados. En instalaciones anteriores de 64 bits de Windows, el proceso reflejaba un subconjunto de las claves del Registro redirigidas entre las vistas de 32 y 64 bits. Sin embargo, la implementación de esto produjo algunas incoherencias en el estado del registro. (Para obtener más información sobre la reflexión del Registro, consulte el artículo de MSDN correspondiente en la sección *Vínculos* a otros recursos a continuación).

A partir Windows 7, hemos quitado completamente la reflexión del Registro y combinado las claves que solían reflejarse:

-   Clases de software HKEY \_ LOCAL \_ MACHINE \\ \\
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ COM3
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ EventSystem
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Ole
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc
-   Clases de software HKEY \_ USERS \\ \* \\ \\
-   Clases HKEY \_ USERS \\ \* \_

De hecho, esto proporciona el mismo comportamiento de reflexión, ya que los cambios en estas claves están disponibles inmediatamente para aplicaciones de 32 y 64 bits.

Las claves reflejadas condicionalmente permanecen divididas:

-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ CLSID
-   Interfaz de clases \_ de software HKEY LOCAL \_ MACHINE \\ \\ \\
-   HKEY \_ USERS Clases de software \\ \* \\ \\ \\ CLSID
-   Interfaz de clases \_ \\ \* \\ de software \\ \\ HKEY USERS
-   \_CLSID de \\ \* \_ clases \\ HKEY USERS
-   Interfaz de clases \_ HKEY USERS \\ \* \_ \\

Se usan para mantener los datos que no se deben compartir entre aplicaciones de 32 y 64 bits.

## <a name="manifestation"></a>Manifestación

Las claves CLSID e Interface de la lista anterior ya no se reflejan mientras se redirigen. Aunque este es el comportamiento deseado en la mayoría de los casos, es posible que las aplicaciones puedan tomar una dependencia de su comportamiento reflejado en Vista.

Las funciones que permiten a las aplicaciones controlar la reflexión (RegDisableReflectionKey y RegEnableReflectionKey) no son operaciones en Windows 7.

## <a name="mitigation-of-impact"></a>Mitigación del impacto

COM es el principal consumidor de la reflexión del Registro. COM y otros consumidores se actualizaron para dar cabida a este cambio. Este cambio no afecta a las aplicaciones que usan las API COM estándar.

## <a name="solution"></a>Solución

Aplique una de las siguientes opciones si se basa en la reflexión del Registro para sincronizar vistas de 32 bits y 64 bits:

-   Creación explícita de claves en ambas vistas durante la instalación
-   Sacar las claves del ámbito de las claves reflejadas
-   Comprobación de ambas vistas del Registro al consultar una clave reflejada

    **Nota:** Las \_ marcas KEY WOW64 \_ 32KEY y KEY \_ WOW64 \_ 64KEY no se pueden combinar

Aplique una de las siguientes opciones si se basa en las funciones RegDisableReflectionKey para deshabilitar la reflexión del Registro:

-   Creación explícita de claves en ambas vistas durante la instalación
-   Sacar las claves del ámbito de las claves reflejadas
-   Usar subclaves específicas de la plataforma (como x86, amd64 e ia64) para separar datos específicos de bits

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Artículo reflexión del Registro](../winprog64/registry-reflection.md)
-   [Lista de claves redirigidas en el artículo Redirector del Registro](../winprog64/registry-redirector.md)
-   [Procedimientos recomendados para Wow64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
