---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Cambios de ordenación de NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0805eae753c1e312d26f8c84e13d19041458cf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546886"
---
# <a name="nls-sorting-changes"></a>Cambios de ordenación de NLS

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes** -Windows XP Windows \| vista Windows \| 7  
**Servidores** : windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** alta  
**Frecuencia** baja (pocas aplicaciones afectadas, pero si se ven afectadas, siempre interrumpidas)  


## <a name="description"></a>Descripción

Las funciones de National Language support (NLS) ayudan a las aplicaciones a satisfacer las distintas necesidades de idioma y de la configuración regional de los usuarios de todo el mundo. Las nuevas versiones de Windows casi invariables incluyen cambios de NLS. Este cambio afecta a la intercalación y la ordenación, y, por lo tanto, a las aplicaciones que tienen índices persistentes.

Una tabla de intercalación tiene dos números que identifican su versión (revisión): la versión definida y la versión NLS. Ambas versiones son valores DWORD, compuesto por una versión principal y una versión secundaria. El primer byte de un valor está reservado, los dos bytes siguientes representan la versión principal y el último byte representa la versión secundaria. En términos hexadecimales, el patrón es 0xRRMMMMmm, donde R es igual a Reserved, M es igual a Major y m es igual a Minor. Por ejemplo, una versión principal de 3 con una versión secundaria de 4 se representa como 0x304.

En el caso de una versión principal, uno o más puntos de código cambian para que la aplicación deba volver a indizar todos los datos para que las comparaciones sean válidas. En el caso de una versión secundaria, no se mueve nada, pero se agregan puntos de código. Para este tipo de versión, la aplicación solo tiene que volver a indexar las cadenas con valores que no se pudieron ordenar previamente. En Resumen, este es el significado de los números de versión en relación con los cambios de datos en las tablas de excepciones específicas de la configuración regional y las tablas predeterminadas:

**NLSVersion principal** : se han modificado los puntos de código de las tablas "excepción" o de configuración regional específicas  
**NLSVersion Minor** : se han agregado nuevos puntos de código en las tablas "Exception" (excepciones) o específicas de la configuración regional.  
**DefinedVersion principal** : cambios de los puntos de código en la tabla predeterminada  
**DefinedVersion Minor** : se han agregado nuevos puntos de código en la tabla predeterminada  


**Ordenar los números de versión de las versiones de lanzamiento:**



| Sistema operativo    | Release           | Versión (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/A: no GetNLSVersion () API |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestación

Las aplicaciones (como bases de datos) con índices persistentes que no comprueben la versión de NLS y vuelvan a indexarse tras el cambio de versión no se podrán ordenar correctamente o puede que no proporcionen los resultados solicitados.

En el caso de las interfaces de usuario, las listas (por ejemplo, alfabético, numérico, alfanumérico, símbolos, etc.) se pueden ordenar de forma incorrecta.

## <a name="solution"></a>Solución

La aplicación puede llamar a **GetNLSVersionEx** (Windows Vista o posterior) o **GetNLSVersion** (anterior a Windows Vista) para recuperar la versión definida y la versión de NLS para una tabla de intercalación.

-   GetNLSVersionEx:

*Recupera información sobre la versión actual de una función NLS especificada para una configuración regional especificada por nombre.*  
Esta función permite a una aplicación como Active Directory determinar si un cambio de NLS afecta a la configuración regional utilizada para una tabla de índice determinada. Si no es así, no es necesario volver a indizar la tabla. Para obtener más información, vea controlar la información regional y de idioma.  
Esta función admite configuraciones regionales personalizadas. Si *lpLocaleName* especifica una configuración regional complementaria, los datos recuperados son los datos correctos para el orden de intercalación asociado a esa configuración regional complementaria.  

**Nota:** Las versiones de Windows anteriores a Windows Vista no admiten **GetNLSVersionEx**.  


-   GetNLSVersion (se usa para aplicaciones que se ejecutan en versiones de Windows anteriores a Windows Vista):

*Recupera información sobre la versión actual de una función NLS especificada para una configuración regional especificada por el identificador*  
Esta función permite a una aplicación como Active Directory determinar si un cambio de NLS afecta al identificador de configuración regional que se usa para una tabla de índice determinada. Si no es así, no es necesario volver a indizar la tabla. Para obtener más información, vea controlar la información regional y de idioma.  
**Nota:** Esta función recupera información solo sobre una configuración regional especificada por el identificador. La función **GetNLSVersionEx** admite configuraciones regionales, características y nombres RFC 4646 adicionales. Sin embargo, las versiones de Windows anteriores a Windows Vista no admiten **GetNLSVersionEx**.  
Las aplicaciones diseñadas para ejecutarse solo en Windows Vista y versiones posteriores deben usar **GetNLSVersionEx** en preferencia a esta función. **GetNLSVersionEx** proporciona una buena compatibilidad para las configuraciones regionales complementarias.  


## <a name="compatibility-test"></a>Prueba de compatibilidad

**Pasos para saber si una versión de intercalación ha cambiado (es decir, es necesario volver a indizar):**

-   **Use GetNLSVersionEx ()** para recuperar una estructura **NLSVERSIONINFOEX** al realizar la indexación original de los datos.
-   Almacene las siguientes propiedades con el índice para identificar la versión:  **NLSVERSIONINFOEX. dwNLSVersion** y **NLSVERSIONINFOEX. dwDefinedVersion** : estas dos propiedades juntas especifican la versión de la tabla de ordenación que está usando.  
    **NLSVERSIONINFOEX. dwEffectiveId** : especifica la configuración regional efectiva de la ordenación. Una configuración regional personalizada apuntará a la ordenación de una configuración regional integrada.  
    
-   Al usar el índice **, use GetNlsVersionEx ()** para detectar la versión de los datos.
-   Si alguna de las tres propiedades ha cambiado, los datos de ordenación que está utilizando podrían devolver resultados diferentes y cualquier indexación que tenga podría no encontrar registros.
-   Si sabe que los datos no contienen puntos de código Unicode no válidos (es decir, todas las cadenas devuelven **true** desde una llamada a **IsNLSDefinedString ()**), puede considerarlas iguales si solo cambió el byte bajo de **dwNLSVersion** y **dwDefinedVersion** (las versiones secundarias descritas anteriormente).

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Internacionalización para aplicaciones para Windows](../intl/international-support.md)
-   [GetNLSVersionEx función)](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion función)](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Cómo saber si la versión de intercalación ha cambiado](/archive/blogs/shawnste/)

 

 
