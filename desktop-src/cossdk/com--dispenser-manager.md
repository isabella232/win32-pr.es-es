---
description: El administrador de dispensadores proporciona agrupación de recursos para los distribuidores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos se da de alta correctamente en la transacción de objetos de aplicación.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Administrador de dispensadores COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec090ba8c6324363c80a00685e4bc9cfa11185fa1b95ad5db3575608c9fe60ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991695"
---
# <a name="com-dispenser-manager"></a>Administrador de dispensadores COM+

El administrador del dispensador proporciona agrupación de recursos para los distribuidores de recursos y garantiza que un recurso proporcionado por un distribuidor de recursos se inste correctamente en la transacción del objeto de aplicación. El administrador del distribuidor reclama automáticamente los recursos que todavía están reservados al final de la duración de un objeto, lo que elimina la posibilidad de "pérdidas" de recursos. El administrador del dispensador puede pedir a un distribuidor de recursos que cree un nuevo recurso o que destruya los recursos inactivos cuando sea necesario para ajustar los niveles de inventario, en lugar de usar la configuración estática.

> [!Note]  
> Dado que no es necesario que las interfaces del dispensador de recursos expuestas a la aplicación sean interfaces COM, el administrador del dispensador se puede usar en un proceso sin inicializar COM, por ejemplo, para admitir el dispensador de recursos ODBC.

 

Tras la creación de recursos, el dispensador de recursos puede especificar cuánto tiempo se permite que un recurso inactivo permanezca en el grupo antes de que se destruya. Un subproceso que se ejecuta en el administrador del distribuidor siempre busca estos recursos inactivos.

## <a name="the-inventory-statistics-manager"></a>Administrador de estadísticas de inventario

El administrador de dispensador usa el administrador *de estadísticas de inventario para* administrar los niveles de inventario de recursos de grupo. El administrador de estadísticas de inventario mantiene un registro de cuándo se usó cada recurso y quita los recursos del inventario cuando no se han usado durante *x* segundos, donde el valor de *x* se establece por recurso cuando se crea el recurso.

## <a name="the-holder-component"></a>Componente Holder

El administrador de dispensador sondea cada *titular,* un componente creado por el administrador de dispensadores que enumera el inventario de recursos para cada distribuidor de recursos, cada 10 segundos para permitirle reajustar su inventario de recursos. Cada titular llama al administrador de estadísticas de inventario para sugerir niveles de inventario para cada tipo de recurso. Como resultado, el titular puede pedir al distribuidor de recursos que cree o destruya algún inventario.

El titular y el distribuidor de recursos se comunican para solicitar recursos de un tipo determinado. Existen las siguientes relaciones entre el titular y el distribuidor de recursos:

-   El titular puede solicitar un recurso al distribuidor de recursos. El distribuidor de recursos devuelve un recurso disponible o crea uno nuevo.
-   El titular puede notificar al distribuidor de recursos que una aplicación ya no necesita un recurso y, a continuación, devolverlo al grupo de recursos.
-   El titular y el distribuidor de recursos trabajan juntos para mantener el tamaño del grupo de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del distribuidor de recursos com+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



