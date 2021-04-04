---
description: En las secciones siguientes se describe el uso de las propiedades de instalador integradas y las propiedades adicionales definidas por el autor del paquete.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilizar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154367"
---
# <a name="using-properties"></a>Utilizar propiedades

En las secciones siguientes se describe el uso de las propiedades de instalador integradas y las propiedades adicionales definidas por el autor del paquete. Las propiedades pueden ser [propiedades públicas](public-properties.md) o [propiedades privadas](private-properties.md). Todas las propiedades que deben definirse al inicializarse el instalador deben tener su nombre y valor inicial enumerados en la [tabla de propiedades](property-table.md). Las propiedades que tienen un valor NULL no se muestran en la tabla de propiedades. Puede obtener o establecer propiedades de programas y acciones personalizadas y establecer propiedades públicas desde la línea de comandos. El proceso de instalación se puede modificar mediante el uso de propiedades en instrucciones condicionales.

[Restricciones en los nombres de propiedad](restrictions-on-property-names.md)

[Inicialización de valores de propiedad](initialization-of-property-values.md)

[Obtener y establecer propiedades](getting-and-setting-properties.md)

[Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)

[Usar una propiedad de directorio en una ruta de acceso](using-a-directory-property-in-a-path.md)

> [!Note]  
> No use propiedades para contraseñas u otra información que deba permanecer segura. El instalador puede escribir el valor de una propiedad creada en la tabla de propiedades o crearla en tiempo de ejecución en un registro o en el registro del sistema.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> </dl>

 

 



