---
description: Un componente calificado es un método de direccionamiento indirecto de un solo nivel, similar a un puntero.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Componentes completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909465"
---
# <a name="qualified-components"></a>Componentes completos

Un componente calificado es un método de direccionamiento indirecto de un solo nivel, similar a un puntero. Los componentes calificados se utilizan principalmente para agrupar componentes con funcionalidad paralela en categorías. Por ejemplo, si tiene 30 componentes enumerados en la [tabla de componentes](component-table.md) que son la misma plantilla de fax de Microsoft Word localizada en 30 idiomas, puede agruparlos en una categoría de componentes calificados mediante la [tabla PublishComponent](publishcomponent-table.md).

Los componentes calificados se escriben en la tabla de componentes de la misma manera que los componentes normales. Cada componente debe tener un GUID de identificador de componente único y un identificador de componente especificado en la tabla de componentes. Además, los componentes completos están asociados a un GUID de categoría y un calificador de cadena de texto en la tabla PublishComponent. El GUID de categoría y el calificador hacen referencia a los componentes calificados, que solo apuntan al componente ordinario de la tabla de componentes.

Por ejemplo, un GUID de identificador de componente calificado puede apuntar a diferentes versiones de idioma de un archivo DLL de recursos. En este caso, el grupo de archivos dll de recursos localizados consta de la categoría y las cadenas de los identificadores de configuración regional (LCID) numéricos se utilizan normalmente como calificadores. Un desarrollador podría crear un paquete de instalación que use estos componentes calificados para hacer lo siguiente:

-   Busque la ruta de acceso a una versión de idioma determinada de la DLL de recursos mediante [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) e instale el recurso.
-   Determine todas las versiones de idioma de la DLL de recursos que están presentes llamando a [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).
-   Prepare la aplicación para admitir otros idiomas. Un paquete de idioma futuro para la aplicación puede utilizar el componente calificado para agregar más versiones de idioma del archivo DLL de recursos.

Para obtener más información, consulte [uso de componentes calificados](using-qualified-components.md).

 

 



