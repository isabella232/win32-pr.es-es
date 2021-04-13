---
description: El administrador dispensador proporciona la agrupación de recursos para los dispensadores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos esté correctamente dado de alta en la transacción de objetos de la aplicación.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Administrador del dispensador de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538836"
---
# <a name="com-dispenser-manager"></a>Administrador del dispensador de COM+

El gestor del dispensador proporciona la agrupación de recursos para los dispensadores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos está correctamente dado de alta en la transacción del objeto de la aplicación. El administrador del dispensador reclama automáticamente los recursos que aún se reservan al final de la duración de un objeto, lo que elimina la posibilidad de que se produzcan pérdidas de recursos. El gestor dispensador puede pedir a un dispensador de recursos que cree un nuevo recurso o destruya los recursos inactivos cuando sea necesario para ajustar los niveles de inventario, en lugar de usar valores estáticos.

> [!Note]  
> Dado que las interfaces dispensadoras de recursos expuestas a la aplicación no deben ser interfaces COM, el administrador dispensador se puede usar en un proceso sin inicializar COM, por ejemplo, para admitir el dispensador de recursos ODBC.

 

Tras la creación de recursos, el dispensador de recursos puede especificar cuánto tiempo se permite que un recurso inactivo permanezca en el grupo antes de que se destruya. Un subproceso que se ejecuta en el administrador dispensador siempre busca estos recursos inactivos.

## <a name="the-inventory-statistics-manager"></a>Administrador de estadísticas de inventario

El gestor del dispensador utiliza el *Administrador de estadísticas de inventario* para administrar los niveles de inventario de recursos del grupo. El administrador de estadísticas de inventario mantiene un registro de Cuándo se usó cada recurso y quita los recursos del inventario cuando no se han usado durante *x* segundos, donde el valor de *x* se establece por recurso cuando se crea el recurso.

## <a name="the-holder-component"></a>Componente de titular

El administrador del dispensador sondea cada *titular*, un componente creado por el administrador del dispensador que muestra el inventario de recursos de cada dispensador de recursos, cada 10 segundos, para que pueda reajustar su inventario de recursos. Cada titular llama a Inventory Statistics Manager para sugerir niveles de inventario para cada tipo de recurso. Como resultado, el titular puede pedir al dispensador de recursos que cree o destruya algún inventario.

El titular y el dispensador de recursos se comunican con los recursos de solicitud de un tipo determinado. Las siguientes relaciones existen entre el titular y el dispensador de recursos:

-   El titular puede solicitar un recurso desde el dispensador de recursos. El dispensador de recursos devuelve un recurso disponible o crea uno nuevo.
-   El titular puede notificar al dispensador de recursos que una aplicación ya no necesita un recurso y, a continuación, devolverlo al grupo de recursos.
-   El titular y el dispensador de recursos trabajan juntos para mantener el tamaño del grupo de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



