---
description: Guardar o descartar cambios
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Guardar o descartar cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01c000a6fc9fbe7e8e25e50c041f1b5a0e1250dfe089245ef035213905e5737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915936"
---
# <a name="saving-or-discarding-changes"></a>Guardar o descartar cambios

Al establecer propiedades en un elemento, no se registra realmente ningún cambio en el catálogo de COM+ hasta que se guarden explícitamente los cambios. Para ello, use [**el método SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el [**objeto COMAdminCatalogCollection**](comadmincatalogcollection.md) de la colección que contiene el elemento.

Si desea descartar los cambios que aún no se han confirmado, puede llamar al método [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) en el [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md) Esto lee todos los datos persistentes del catálogo de COM+ para todos los elementos de la colección, eliminando eficazmente los cambios pendientes.

Cuando se usa [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), las incoherencias en la configuración de propiedades que haya elegido producirán un error y **SaveChanges** no podrá escribir el objeto que devolvió el error. Todas las propiedades de un elemento determinado se escriben o no se escriben como un todo.

Sin embargo, cuando se producen errores de escritura, es posible que no se deba a una configuración incompatible; es posible que se haya producido algún otro error. Debe inspeccionar los detalles del error para estar seguros. Para obtener más información, vea [Control de errores de administración de COM+](handling-com--administration-errors.md) e [interdependencias entre propiedades](interdependencies-between-properties.md).

Como regla general, cuanto más cambios intente guardar a la vez, especialmente los cambios en varios objetos, más probable es que obtenga un error y más difícil sea realizar el seguimiento.

Además, entre las llamadas [**a Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), no tiene ningún bloqueo en los elementos de la colección; la contención es posible. Para obtener más información, vea [Getting and Setting Properties](getting-and-setting-properties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y establecer propiedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependencias entre propiedades](interdependencies-between-properties.md)
</dt> <dt>

[Consulta de propiedades disponibles](querying-for-available-properties.md)
</dt> </dl>

 

 



