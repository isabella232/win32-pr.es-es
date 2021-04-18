---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Eliminación de la reflexión del registro de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707119"
---
# <a name="removal-of-windows-registry-reflection"></a>Eliminación de la reflexión del registro de Windows

## <a name="platform"></a>Plataforma

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

El proceso de reflexión del registro copia las claves y los valores del registro entre dos vistas del registro para mantenerlas sincronizadas. En las instalaciones anteriores de 64 bits de Windows, el proceso reflejaba un subconjunto de las claves del registro Redirigido entre las vistas de 32 bits y de 64 bits. Sin embargo, la implementación de esto causó algunas incoherencias en el estado del registro. (Para obtener más información sobre la reflexión del registro, consulte el artículo de MSDN correspondiente en la sección *vínculos a otros recursos* a continuación).

A partir de Windows 7, hemos quitado la reflexión del registro por completo y combinado las claves que solían reflejarse:

-   HKEY \_ \_ clases de \\ software de máquina local \\
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ com3
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ EventSystem
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC
-   \_Clases de \\ \* \\ software \\ de usuarios HKEY
-   \_Clases de usuarios HKEY \\ \* \_

De hecho, esto proporciona el mismo comportamiento de reflexión, ya que los cambios en estas claves inmediatamente están disponibles para las aplicaciones de 32 y 64 bits.

Las claves que se reflejaron condicionalmente permanecen divididas:

-   HKEY \_ \_ clases de software de máquina local \\ \\ \\ CLSID
-   HKEY \_ \_ interfaz de \\ clases de software de máquina \\ local \\
-   \_Clases de software de usuarios HKEY \\ \* \\ \\ \\ CLSID
-   La \_ \\ \* \\ interfaz de \\ clases de software \\ de usuarios HKEY
-   \_Clases de usuarios HKEY \\ \* \_ \\ CLSID
-   \_Clase HKEY users ( \\ \* \_ \\ interfaz)

Se usan para mantener los datos que no se deben compartir entre las aplicaciones de 32 bits y 64 bits.

## <a name="manifestation"></a>Manifestación

Las claves CLSID y de interfaz de la lista anterior no se reflejan ya mientras se redirigen. Aunque este es el comportamiento deseado en la mayoría de los casos, es posible que las aplicaciones tomen una dependencia del comportamiento reflejado en vista.

Las funciones que permiten a las aplicaciones controlar la reflexión (RegDisableReflectionKey y RegEnableReflectionKey) no son operaciones en Windows 7.

## <a name="mitigation-of-impact"></a>Mitigación del impacto

COM es el consumidor principal de la reflexión del registro. COM y otros consumidores se actualizaron para dar cabida a este cambio. Este cambio no afecta a las aplicaciones que usan las API COM estándar.

## <a name="solution"></a>Solución

Aplique una de las siguientes opciones si se basa en la reflexión del registro para sincronizar las vistas de 32 bits y 64 bits:

-   Crear claves en ambas vistas explícitamente durante la instalación
-   Sacar las claves del ámbito de las claves reflejadas
-   Comprobar ambas vistas del registro cuando se consulta una clave reflejada

    **Nota:** \_No se \_ \_ pueden combinar las marcas de 32KEY de la clave WOW64 y 64KEY de la clave WOW64 \_

Aplique una de las siguientes opciones si confía en las funciones de RegDisableReflectionKey para deshabilitar la reflexión del registro:

-   Crear claves en ambas vistas explícitamente durante la instalación
-   Sacar las claves del ámbito de las claves reflejadas
-   Usar subclaves específicas de la plataforma (como x86, AMD64 e ia64) para separar datos específicos de bits

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Artículo sobre la reflexión del registro](../winprog64/registry-reflection.md)
-   [Lista de claves redirigidas en el artículo redirector del registro](../winprog64/registry-redirector.md)
-   [Prácticas recomendadas para WOW64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
