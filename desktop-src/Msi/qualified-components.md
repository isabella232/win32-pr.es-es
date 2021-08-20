---
description: Un componente calificado es un método de direccionamiento indirecto de un solo nivel, similar a un puntero.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Componentes calificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c9a5ccd757516402a951afa3a105d51e3a0b3d22a88614983997dbcd6d07f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376308"
---
# <a name="qualified-components"></a>Componentes calificados

Un componente calificado es un método de direccionamiento indirecto de un solo nivel, similar a un puntero. Los componentes calificados se usan principalmente para agrupar componentes con funcionalidad paralela en categorías. Por ejemplo, si tiene 30 [](component-table.md) componentes enumerados en la tabla Componentes que son la misma plantilla de fax de Microsoft Word localizada en 30 idiomas, puede agrupar estos componentes en una categoría de componentes calificados mediante la [tabla PublishComponent](publishcomponent-table.md).

Los componentes calificados se introducen en la tabla Component de la misma manera que los componentes normales. Cada componente debe tener un GUID de identificador de componente único y un identificador de componente especificados en la tabla Component. Además, los componentes calificados están asociados a un GUID de categoría y un calificador de cadena de texto en la tabla PublishComponent. El GUID de categoría y el calificador hacen referencia a los componentes calificadores, que solo apuntan al componente normal de la tabla Component.

Por ejemplo, un GUID de identificador de componente calificado puede apuntar a diferentes versiones de lenguaje de un archivo DLL de recursos. En este caso, el grupo de archivos DLL de recursos localizados consta de la categoría y las cadenas de identificadores de configuración regional numéricos (LCID) se usan normalmente como calificadores. Un desarrollador podría crear un paquete de instalación que use estos componentes calificados para hacer lo siguiente:

-   Busque la ruta de acceso a una versión de lenguaje determinada del archivo DLL de recursos mediante [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) e instale el recurso.
-   Determine todas las versiones de lenguaje del archivo DLL de recursos que están presentes llamando a [**MsiEnumComponentQualifiers.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
-   Prepare la aplicación para admitir idiomas adicionales. Un paquete de idioma futuro para la aplicación puede usar el componente calificado para agregar más versiones de idioma del archivo DLL de recursos.

Para obtener más información, [vea Usar componentes calificados.](using-qualified-components.md)

 

 



