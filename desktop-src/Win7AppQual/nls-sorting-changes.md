---
description: Cambios de ordenación de NLS
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Cambios de ordenación de NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088063"
---
# <a name="nls-sorting-changes"></a>Cambios de ordenación de NLS

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** alta  
**Frecuencia:** baja (pocas aplicaciones afectadas, pero si se afectan, siempre se rompen)  


## <a name="description"></a>Descripción

Las funciones de compatibilidad con idiomas nacionales (NLS) ayudan a las aplicaciones a satisfacer las distintas necesidades específicas del idioma y la configuración regional de los usuarios de todo el mundo. Las nuevas versiones de Windows incluyen casi invariablemente cambios de NLS. Este cambio afecta a la intercalación y la ordenación y, por tanto, a las aplicaciones que tienen índices persistentes.

Una tabla de intercalación tiene dos números que identifican su versión (revisión): la versión definida y la versión nls. Ambas versiones son valores DWORD, compuestos por una versión principal y una versión secundaria. El primer byte de un valor está reservado, los dos bytes siguientes representan la versión principal y el último byte representa la versión secundaria. En términos hexadecimales, el patrón es 0xRRMMMMmm, donde R es igual a Reservado, M es igual a principal y m es menor. Por ejemplo, una versión principal de 3 con una versión secundaria de 4 se representa como 0x304.

Para una versión principal, uno o varios puntos de código cambian para que la aplicación deba volver a indexar todos los datos para que las comparaciones sean válidas. Para una versión secundaria, no se mueve nada, pero se agregan puntos de código. Para este tipo de versión, la aplicación solo tiene que volver a indexar las cadenas con valores no disponibles previamente. En resumen, esto es lo que significan los números de versión en relación con los cambios de datos en las tablas de excepciones específicas de la configuración regional y las tablas predeterminadas:

**NLSVersion Major:** se han cambiado los puntos de código en las tablas "exception" o específicas de la configuración regional.  
**NLSVersion Minor:** se han agregado nuevos puntos de código en las tablas "exception" o específicas de la configuración regional.  
**DefinedVersion Major:** se han cambiado los puntos de código en la tabla predeterminada.  
**DefinedVersion Minor:** se han agregado nuevos puntos de código en la tabla predeterminada.  


**Ordenar los números de versión de las versiones publicadas:**



| Sistema operativo    | Release           | Versión (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/A: ninguna API GetNLSVersion() |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestación

Las aplicaciones (como las bases de datos) con índices persistentes que no comprueban la versión de NLS y se indexan de nuevo tras el cambio de versión no se ordenan correctamente o pueden no proporcionar los resultados solicitados.

En el caso de las interfaces de usuario, las listas (por ejemplo, alfabéticas, numéricas, alfanuméricas, símbolos, entre otras) pueden ordenarse incorrectamente.

## <a name="solution"></a>Solución

La aplicación puede llamar a **GetNLSVersionEx** (Windows Vista o posterior) o **GetNLSVersion** (antes de Windows Vista) para recuperar la versión definida y la versión NLS de una tabla de intercalación.

-   GetNLSVersionEx:

*Recupera información sobre la versión actual de una funcionalidad de NLS especificada para una configuración regional especificada por nombre.*  
Esta función permite a una aplicación como Active Directory determinar si un cambio de NLS afecta a la configuración regional usada para una tabla de índice determinada. Si no es así, no es necesario volver a indexar la tabla. Para obtener más información, vea Control de la configuración regional y la información de idioma.  
Esta función admite configuraciones regionales personalizadas. Si *lpLocaleName especifica* una configuración regional complementaria, los datos recuperados son los datos correctos para el orden de intercalación asociado a esa configuración regional complementaria.  

**Nota:** Las versiones de Windows anteriores a Windows Vista no **admiten GetNLSVersionEx**.  


-   GetNLSVersion (se usa para aplicaciones que se ejecutan en versiones de Windows anteriores a Windows Vista):

*Recupera información sobre la versión actual de una funcionalidad de NLS especificada para una configuración regional especificada por el identificador.*  
Esta función permite a una aplicación como Active Directory determinar si un cambio de NLS afecta al identificador de configuración regional utilizado para una tabla de índice determinada. Si no es así, no es necesario volver a indexar la tabla. Para obtener más información, vea Control de la configuración regional y la información de idioma.  
**Nota:** Esta función recupera información solo sobre una configuración regional especificada por identifier. La **función GetNLSVersionEx** admite configuraciones regionales, características y nombres RFC 4646 adicionales. Sin embargo, las versiones de Windows anteriores a Windows Vista no **admiten GetNLSVersionEx**.  
Las aplicaciones pensadas para ejecutarse solo en Windows Vista y versiones posteriores deben **usar GetNLSVersionEx** en lugar de esta función. **GetNLSVersionEx proporciona** una buena compatibilidad con configuraciones regionales complementarias.  


## <a name="compatibility-test"></a>Prueba de compatibilidad

**Pasos para saber si ha cambiado una versión de intercalación (es decir, debe volver a indexar):**

-   **Use GetNLSVersionEx()** para recuperar una estructura **NLSVERSIONINFOEX** al realizar la indexación original de los datos.
-   Almacene las siguientes propiedades con el índice para identificar la versión:  **NLSVERSIONINFOEX.dwNLSVersion** y **NLSVERSIONINFOEX.dwDefinedVersion:** estas dos propiedades juntos especifican la versión de la tabla de ordenación que está usando.  
    **NLSVERSIONINFOEX.dwEffectiveId:** especifica la configuración regional efectiva de su ordenación. Una configuración regional personalizada apuntará a la ordenación de una configuración regional en el cuadro.  
    
-   Al usar el índice, **use GetNlsVersionEx()** para detectar la versión de los datos.
-   Si alguna de las tres propiedades ha cambiado, los datos de ordenación que está usando podrían devolver resultados diferentes y cualquier indexación que tenga podría no encontrar registros.
-   Si sabe que los datos no contienen puntos de código Unicode no válidos (es decir, todas las cadenas devolvieron **TRUE** desde una llamada a **IsNLSDefinedString()**), puede considerarlos iguales si solo ha cambiado el byte inferior de **dwNLSVersion** y **dwDefinedVersion** (las versiones secundarias descritas anteriormente).

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Internacionalización para aplicaciones para Windows](../intl/international-support.md)
-   [GetNLSVersionEx (Función)](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion (Función)](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Cómo saber si ha cambiado la versión de intercalación](/archive/blogs/shawnste/)

 

 
