---
description: El administrador de dispensador proporciona agrupación de recursos para los dispensadores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos se inseleccione correctamente en la transacción de objetos de aplicación.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Administrador de dispensadores COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476109"
---
# <a name="com-dispenser-manager"></a>Administrador de dispensadores COM+

El administrador de dispensador proporciona agrupación de recursos para los dispensadores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos se inseleccione correctamente en la transacción del objeto de aplicación. El administrador de dispensador reclama automáticamente los recursos que todavía están reservados al final de la duración de un objeto, lo que elimina la posibilidad de "pérdidas" de recursos. El administrador del dispensador puede pedir a un dispensador de recursos que cree un nuevo recurso o que destruya los recursos inactivos cuando sea necesario para ajustar los niveles de inventario, en lugar de usar la configuración estática.

> [!Note]  
> Dado que no es necesario que las interfaces de dispensador de recursos expuestas a la aplicación sean interfaces COM, el administrador del dispensador se puede usar en un proceso sin inicializar COM, por ejemplo, para admitir el dispensador de recursos ODBC.

 

Tras la creación del recurso, el dispensador de recursos puede especificar cuánto tiempo se permite que un recurso inactivo permanezca en el grupo antes de que se destruya. Un subproceso que se ejecuta en el administrador de dispensador siempre busca estos recursos inactivos.

## <a name="the-inventory-statistics-manager"></a>Administrador de estadísticas de inventario

El administrador de dispensador usa el administrador *de estadísticas de inventario para* administrar los niveles de inventario de recursos de grupo. El administrador de estadísticas de inventario mantiene un registro de cuándo se usó cada recurso y quita los recursos del inventario cuando no se han usado durante *x* segundos, donde el valor de *x* se establece por recurso cuando se crea el recurso.

## <a name="the-holder-component"></a>Componente Holder

El administrador de dispensador sondea cada *titular,* un componente creado por el administrador del dispensador que enumera el inventario de recursos para cada dispensador de recursos, cada 10 segundos para permitirle reajustar su inventario de recursos. Cada titular llama al administrador de estadísticas de inventario para sugerir niveles de inventario para cada tipo de recurso. Como resultado, el titular puede pedir al dispensador de recursos que cree o destruya algún inventario.

El titular y el dispensador de recursos se comunican para solicitar recursos de un tipo determinado. Existen las siguientes relaciones entre el titular y el dispensador de recursos:

-   El titular puede solicitar un recurso del dispensador de recursos. El dispensador de recursos devuelve un recurso disponible o crea uno nuevo.
-   El titular puede notificar al dispensador de recursos que una aplicación ya no necesita un recurso y, a continuación, devolverlo al grupo de recursos.
-   El titular y el dispensador de recursos funcionan conjuntamente para mantener el tamaño del grupo de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos com+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



