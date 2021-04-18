---
description: 'Windows Vista y versiones posteriores: NLS define varias configuraciones regionales que se usan además de las configuraciones regionales de Windows existentes.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686717"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista y versiones posteriores:** NLS define varias configuraciones regionales que se usan además de las configuraciones regionales de Windows existentes. Use estas pseudo-configuraciones regionales para probar la localización de las aplicaciones. Para obtener información detallada sobre la implementación, consulte [uso de Pseudo-Locales para las pruebas de localización](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Pseudo-Locales admitidos

Las pseudo configuraciones regionales admitidas por NLS son:

-   Pseudo-configuración regional
-   Pseudo-configuración regional reflejada (de derecha a izquierda)
-   Sudeste asiático-idioma

Elija la configuración regional específica que se va a usar en función de las asignaciones de páginas de códigos y las cadenas para la localización; por ejemplo, los nombres de los meses y los días. Los datos de cada pseudo-configuración regional incluyen no solo las páginas de códigos relevantes y las cadenas de día y mes para la localización, sino también los datos de otros casos de prueba para NLS. Los casos de prueba examinan los siguientes tipos de datos:

-   [identificadores de configuración regional](locale-identifiers.md)de 9 bits. Las pseudo-configuraciones regionales proporcionan una buena oportunidad para probar el funcionamiento de los identificadores de configuración regional de 9 bits.
-   Cadenas de lenguajes que deben usar fuentes pequeñas. Debido a las limitaciones de la interfaz de dispositivo gráfico (GDI), la fuente de la interfaz de usuario para algunos idiomas es más pequeña que la óptima. Las configuraciones regionales incluyen varias cadenas de estos lenguajes, combinadas con cadenas de idiomas con control de fuentes más estándar. Puede utilizar estas cadenas en las pruebas para determinar cómo se representa una fuente limitada por GDI.
-   Longitudes de cadena inusuales. Algunas constantes de información de configuración regional, por ejemplo, la [configuración regional \_ SLIST](locale-slist.md) y la [configuración regional \_ ICURRENCY](locale-icurrency.md), tienen límites convencionales en el tamaño de la cadena. Las pseudo configuraciones regionales admiten el examen de longitudes de cadena variables.
-   Ordenaciones alternativas. Las pseudo configuraciones regionales se pueden usar para probar la funcionalidad de ordenación alternativa cuando el identificador de criterio de [ordenación](sort-order-identifiers.md) alternativo difiere del identificador de criterio de ordenación base que normalmente está asociado a la configuración regional.

## <a name="pseudo-locale-names-and-identifiers"></a>Nombres e identificadores de pseudo-configuración regional

Las pseudo-configuraciones regionales tienen [nombres de configuración regional](locale-names.md) que se eligen en el espacio de uso privado para evitar conflictos con las posibles cadenas introducidas en los estándares organización internacional de normalización (iso) 639 e ISO 3166. Cada pseudo-configuración regional también tiene su propio identificador de configuración regional. En la tabla siguiente se proporcionan los nombres y los identificadores de las pseudo configuraciones regionales definidas.



| Pseudo-configuración regional       | Nombre de configuración regional | Identificador de configuración regional |
|---------------------|-------------|-------------------|
| Base                | QPS-PLOC    | 0501              |
| Reflejado            | QPS-plocm   | 09ff              |
| Idioma asiático oriental | QPS-Ploca   | 05fe              |



 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el texto que se muestra para una seudoclase de base:

\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ! \] ōf 2006

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Identificadores de configuración regional](locale-identifiers.md)
</dt> <dt>

[Nombres de configuración regional](locale-names.md)
</dt> <dt>

[Identificadores de criterio de ordenación](sort-order-identifiers.md)
</dt> <dt>

[Usar Pseudo-Locales para las pruebas de localización](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



