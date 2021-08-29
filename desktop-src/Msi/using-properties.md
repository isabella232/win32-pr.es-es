---
description: En las secciones siguientes se describe el uso de las propiedades del instalador integradas y las propiedades adicionales definidas por el autor del paquete.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilizar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d0fda0c3be64c6441a6de6c870838406dddd608fe6fa87665407e720c8d7d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499205"
---
# <a name="using-properties"></a>Utilizar propiedades

En las secciones siguientes se describe el uso de las propiedades del instalador integradas y las propiedades adicionales definidas por el autor del paquete. Las propiedades pueden ser [propiedades públicas o](public-properties.md) [privadas.](private-properties.md) Todas las propiedades que deben definirse tras la inicialización del instalador deben tener su nombre y valor inicial enumerados en la [tabla Property](property-table.md). Las propiedades que tienen un valor NULL no se muestran en la tabla Property. Puede obtener o establecer propiedades de programas y acciones personalizadas y establecer propiedades públicas desde la línea de comandos. El proceso de instalación se puede modificar mediante el uso de propiedades en instrucciones condicionales.

[Restricciones en los nombres de propiedad](restrictions-on-property-names.md)

[Inicialización de valores de propiedad](initialization-of-property-values.md)

[Obtener y establecer propiedades](getting-and-setting-properties.md)

[Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)

[Usar una propiedad de directorio en una ruta de acceso](using-a-directory-property-in-a-path.md)

> [!Note]  
> No use propiedades para contraseñas u otra información que deba permanecer segura. El instalador puede escribir el valor de una propiedad creada en la tabla Property o creada en tiempo de ejecución en un registro o en el registro del sistema.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> </dl>

 

 



