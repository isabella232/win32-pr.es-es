---
description: Guardar o descartar cambios
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Guardar o descartar cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907090"
---
# <a name="saving-or-discarding-changes"></a>Guardar o descartar cambios

Cuando se establecen propiedades en un elemento, en realidad no se registra ningún cambio en el catálogo de COM+ hasta que se guardan los cambios explícitamente. Para ello, use el método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para la colección que contiene el elemento.

Si desea descartar los cambios que aún no se han confirmado, puede llamar al método de [**rellenado**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Esto Lee todos los datos persistentes del catálogo de COM+ para todos los elementos de la colección, con lo que se eliminan eficazmente los cambios pendientes.

Cuando se utiliza [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), las incoherencias en la configuración de propiedades que ha elegido producen un error y **SaveChanges** no puede escribir el objeto que devolvió el error. Todas las propiedades de un elemento determinado se escriben o no se escriben en su totalidad.

Sin embargo, cuando se producen errores de escritura, es posible que no se deba a una configuración incompatible. es posible que se haya producido algún otro error. Debe inspeccionar los detalles del error para estar seguro. Para obtener más información, consulte [controlar errores de administración de com+](handling-com--administration-errors.md) e [interdependencias entre propiedades](interdependencies-between-properties.md).

Como norma general, cuanto más cambios intente guardar a la vez, especialmente en el hecho de que se produzcan cambios en varios objetos, más probabilidades de que obtenga un error y más difícil sea hacer un seguimiento.

Además, entre las llamadas a [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), no hay ningún bloqueo en los elementos de la colección; es posible la contención. Para obtener más información, vea [obtener y establecer propiedades](getting-and-setting-properties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y establecer propiedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependencias entre propiedades](interdependencies-between-properties.md)
</dt> <dt>

[Consultar las propiedades disponibles](querying-for-available-properties.md)
</dt> </dl>

 

 



