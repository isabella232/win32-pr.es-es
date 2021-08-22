---
description: Para generar un módulo de combinación, debe obtener una herramienta de software con la que editar un archivo .msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtener herramientas de creación de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a85fb75c0317a6737393e67f12a7a03cd8b76c68a8261c9d26d10d06cbe484c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327885"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Obtener herramientas de creación de módulos de mezcla

Para generar un módulo de combinación, debe obtener una herramienta de software con la que editar un archivo .msm. Dado que un archivo .msm es básicamente un archivo .msi simplificado, puede usar las mismas herramientas que se usan para crear una base de datos de instalación. Por ejemplo, la aplicación Orca.exe con el SDK Windows Installer.

Una alternativa es comprar una de las herramientas de empaquetado del instalador para que esté disponible para proveedores de software independientes. Hay varias herramientas de terceros en desarrollo que se pueden usar para generar módulos de combinación. Si decide usar una herramienta de terceros, debe comprobar que genera módulos de combinación coherentes con el estándar descrito en este documento. En concreto, debe determinar que las herramientas de edición no han realizado ninguna de las siguientes acciones en el módulo de combinación.

-   Se han agregado tablas externas al módulo de combinación a las que no se hace referencia en la [tabla ModuleIgnoreTable](moduleignoretable-table.md).

    Elimine estas tablas o agrégrélas a la tabla ModuleIgnoreTable.

-   Se ha agregado una tabla [TextStyle innecesaria](textstyle-table.md) al módulo merge.

    Si el módulo de combinación no tiene interfaz de usuario (y por lo general no debería hacerlo), puede eliminar esta tabla de forma segura.

-   Se han agregado entradas innecesarias a la [tabla Directory](directory-table.md).

    Quite las entradas innecesarias de la tabla Directory.

-   Se ha dejado información fuera de la tabla \_ Validación del módulo de mezcla.

    Esto evita la validación del módulo de mezcla. Agregue una tabla \_ de validación completa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de interfaces de usuario en módulos de combinación](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Creación de tablas de directorios de módulos de mezcla](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Validación de módulos de combinación](validating-merge-modules.md)
</dt> </dl>

 

 



