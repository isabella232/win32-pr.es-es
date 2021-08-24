---
description: 'Windows Vista y versiones posteriores: NLS define varias pseudo-configuraciones regionales para su uso además de las configuraciones regionales Windows existentes.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e099ee2af283c38aff3de7813fec64b5d43c6ac5873549856b27fd224c3e0d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390419"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista y versiones posteriores:** NLS define varias pseudo-configuraciones regionales para su uso además de las configuraciones regionales Windows existentes. Use estas pseudo-configuraciones regionales para probar la localización de las aplicaciones. Para obtener detalles de implementación, [vea Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Compatible Pseudo-Locales

Las pseudo-configuraciones regionales admitidas por NLS son:

-   Pseudo-configuración regional base
-   Pseudo-configuración regional reflejada (de derecha a izquierda)
-   Pseudo-configuración regional del este de Asia

Elija la pseudo-configuración regional concreta que se usará en función de sus asignaciones de página de códigos y las cadenas para la localización, por ejemplo, nombres de mes o nombres de día. Los datos de cada pseudo-configuración regional incluyen no solo páginas de códigos relevantes y cadenas de día y mes para la localización, sino también datos para otros casos de prueba para NLS. Los casos de prueba examinan los siguientes tipos de datos:

-   Identificadores de configuración [regional de](locale-identifiers.md)9 bits . Las pseudo-configuraciones regionales proporcionan una buena oportunidad para probar el funcionamiento de los identificadores de configuración regional de 9 bits.
-   Cadenas de idiomas que deben usar fuentes pequeñas. Debido a las limitaciones de la interfaz de dispositivo gráfico (GDI), la fuente de la interfaz de usuario para algunos lenguajes es menor que la óptima. Las pseudo-configuraciones regionales incluyen varias cadenas de estos idiomas, combinadas con cadenas de idiomas con un control de fuentes más estándar. Puede usar estas cadenas en las pruebas para determinar cómo se representa una fuente limitada por GDI.
-   Longitudes de cadena inusuales. Algunas constantes de información de configuración regional, por ejemplo, [LOCALE \_ SLIST](locale-slist.md) y [LOCALE \_ ICURRENCY](locale-icurrency.md), tienen límites convencionales en el tamaño de cadena. Las pseudo-configuraciones regionales admiten el examen de longitudes de cadenas variadas.
-   Ordenaciones alternativas. Las pseudo-configuraciones regionales se pueden [](sort-order-identifiers.md) usar para probar la funcionalidad de ordenación alternativa cuando el identificador de criterio de ordenación alternativo difiere del identificador de criterio de ordenación base que normalmente está asociado a la configuración regional.

## <a name="pseudo-locale-names-and-identifiers"></a>Nombres e identificadores de pseudo-configuración regional

Las pseudo-configuraciones regionales tienen nombres de configuración regional que se eligen en el espacio de uso privado para evitar conflictos con las posibles cadenas introducidas en los estándares Organización internacional de normalización (ISO) 639 e ISO 3166. [](locale-names.md) Cada pseudo-configuración regional también tiene su propio identificador de configuración regional. En la tabla siguiente se proporcionan los nombres e identificadores de las pseudo-configuraciones regionales definidas.



| Pseudo-configuración regional       | Nombre de la configuración regional | Identificador de configuración regional |
|---------------------|-------------|-------------------|
| Base                | qps-ploc    | 0501              |
| Reflejado            | qps-quécm   | 09ff              |
| Idioma asiático oriental | qps-quéca   | 05fe              |



 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el texto que se muestra para una pseudo-configuración regional base:

\[Шěđлеśđαỳ !!! , \] 8 \[ Μäŕςћ ! \] öf 2006

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

[Uso de Pseudo-Locales para las pruebas de localización](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



