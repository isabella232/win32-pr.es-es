---
description: Uso de datos de configuración regional persistentes
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Uso de datos de configuración regional persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913694"
---
# <a name="using-persistent-locale-data"></a>Uso de datos de configuración regional persistentes

Una aplicación globalizada suele persistir o transmitir datos, por ejemplo, la hora y la fecha. A la hora de decidir cómo debe controlar la aplicación la persistencia de los datos, recuerde que no se garantiza que los datos sean los mismos desde un equipo a otro o entre las ejecuciones de la aplicación. Esto se aplica a las [configuraciones regionales](locales-and-languages.md) que se envían con Windows y a las [configuraciones regionales personalizadas](custom-locales.md).

El diseño de la aplicación debe tener en cuenta una serie de cambios en los datos relacionados con la configuración regional que se pueden producir. Por ejemplo:

-   Los símbolos de moneda pueden cambiar a medida que los países adoptan el euro.
-   Las preferencias regionales pueden cambiar. Por ejemplo, el formato d/m/y puede cambiar al formato m/d/y para una configuración regional determinada.
-   La ortografía de los nombres de los días puede cambiar debido a las reformas de la ortografía. Además, el uso de mayúsculas y minúsculas puede cambiar para los nombres de mes o día.

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>Usar formatos de Locale-Independent para el almacenamiento y el intercambio de datos

Una aplicación que conserva los datos debe usar formatos independientes de la configuración regional para el almacenamiento y el intercambio de datos. Algunos ejemplos son los formatos codificados de forma rígida o estándar. el [nombre de configuración regional de configuración \_ \_ ](locale-name-constants.md)regional invariable y los formatos de almacenamiento binario.

Si se requieren datos de ordenación persistentes, la aplicación debe usar la función [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) . Recuerde que un formato invariable no permanece invariable para la [ordenación](sorting.md), solo para los datos de la configuración regional y del calendario.

## <a name="use-the-user-default-locale-for-data-presentation"></a>Usar la configuración regional predeterminada del usuario para la presentación de datos

Para presentar datos persistentes, lo mejor es que la aplicación vuelva a dar formato a los datos mediante la configuración regional predeterminada del usuario. El uso de esta configuración regional permite invalidaciones del usuario. Para obtener más información, vea [configuración \_ \_ predeterminada de usuario regional](locale-user-default.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Configuraciones regionales personalizadas](custom-locales.md)
</dt> <dt>

[Ordenación](sorting.md)
</dt> </dl>

 

 



