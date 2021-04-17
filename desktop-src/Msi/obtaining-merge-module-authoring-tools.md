---
description: Para generar un módulo de combinación, debe obtener una herramienta de software con la que editar un archivo. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtener herramientas de creación de módulos de fusión mediante combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677533"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Obtener herramientas de creación de módulos de fusión mediante combinación

Para generar un módulo de combinación, debe obtener una herramienta de software con la que editar un archivo. msm. Dado que un archivo. MSM es básicamente un archivo. msi simplificado, es posible que pueda usar las mismas herramientas que se usan para crear una base de datos de instalación. Por ejemplo, la aplicación Orca.exe proporciona con el SDK de Windows Installer.

Una alternativa es adquirir una de las herramientas de empaquetado del instalador para que esté disponible en proveedores de software independientes. Hay varias herramientas de terceros en desarrollo que se pueden usar para generar módulos de combinación. Si decide usar una herramienta de terceros, debe comprobar que genera módulos de combinación que son coherentes con el estándar descrito en este documento. En concreto, debe determinar que las herramientas de edición no han realizado ninguno de los elementos siguientes en el módulo de combinación.

-   Se han agregado tablas extrañas al módulo de combinación al que no se hace referencia en la [tabla ModuleIgnoreTable](moduleignoretable-table.md).

    Elimine estas tablas o agréguelas a la tabla ModuleIgnoreTable.

-   Se ha agregado una [tabla TextStyle](textstyle-table.md) no necesaria al módulo de combinación.

    Si el módulo de combinación no tiene ninguna interfaz de usuario (y generalmente no debería hacerlo) puede eliminar esta tabla de forma segura.

-   Se han agregado entradas innecesarias a la [tabla de directorio](directory-table.md).

    Quite las entradas innecesarias de la tabla de directorio.

-   Información izquierda de la tabla de validación del módulo de combinación \_ .

    Esto evita la validación del módulo de combinación. Agregue una \_ tabla de validación completa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear interfaces de usuario en módulos de combinación](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Crear tablas del directorio del módulo de combinación](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Validar módulos de combinación](validating-merge-modules.md)
</dt> </dl>

 

 



