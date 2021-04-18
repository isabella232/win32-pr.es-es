---
description: Dado que una acción personalizada se puede programar en las tablas de la interfaz de usuario y de secuencia de ejecución, y se puede ejecutar en el proceso del servicio o del cliente, una acción personalizada puede ejecutarse varias veces.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opciones de programación de la ejecución de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667623"
---
# <a name="custom-action-execution-scheduling-options"></a>Opciones de programación de la ejecución de acciones personalizadas

Dado que una acción personalizada se puede programar en las tablas de la interfaz de usuario y de secuencia de ejecución, y se puede ejecutar en el proceso del servicio o del cliente, una acción personalizada puede ejecutarse varias veces.

Tenga en cuenta que el instalador:

-   Ejecuta inmediatamente las acciones en una tabla de secuencia de forma predeterminada.
-   No ejecuta una acción si el campo de expresión condicional de la tabla de secuencia se evalúa como false.
-   Procesa la tabla de la secuencia de la interfaz de usuario en el proceso de cliente si el nivel de interfaz del usuario interno está establecido en el modo de interfaz de usuario completa (vea [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obtener una descripción de los niveles de IU).
-   Es un servicio registrado de forma predeterminada cuando se usa Windows 2000 y, en este caso, la tabla de secuencia de ejecución se procesa en el servicio de instalador.

Puede utilizar las siguientes marcas de opciones para controlar la ejecución inmediata de acciones personalizadas. Para establecer una opción, agregue el valor de esta tabla al valor del campo Type de la [tabla CustomAction](customaction-table.md). No se debe usar ninguna de las marcas siguientes con [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md).

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>predeterminada
</dt> <dd>

Hexadecimal: 0x00000000

Decimal: 0

Ejecutar siempre. La acción se puede ejecutar dos veces si está presente en ambas tablas de secuencia.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Hexadecimal: 0x00000100

Decimal: 256

No ejecute más de una vez si está presente en ambas tablas de secuencia. Siempre omite la acción en la secuencia de ejecución si se ha ejecutado la secuencia de la interfaz de usuario. Ningún efecto en la secuencia de la interfaz de usuario. No es necesario que la acción esté presente o se ejecute en la secuencia de IU que se va a omitir en la secuencia de ejecución. No se ve afectado por la instalación del registro del servicio.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Hexadecimal: 0x00000200

Decimal: 512

Se ejecuta una vez por proceso, en ambas tablas de secuencia. Omite la acción en la secuencia de ejecución si la secuencia de la interfaz de usuario se ha ejecutado en el mismo proceso, por ejemplo, ambas se ejecutan en el proceso del cliente. Se utiliza para evitar que las acciones que modifican el estado de sesión, como datos de propiedades y de base de datos, se ejecuten dos veces.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Hexadecimal: 0x00000300

Decimal: 768

Ejecutar solo si se ejecuta en el cliente después de ejecutar la secuencia de la interfaz de usuario. La acción se ejecuta solo si la secuencia de ejecución se ejecuta en el cliente después de la secuencia de la interfaz de usuario. Se puede usar para proporcionar la lógica/o, o para suprimir el procesamiento relacionado con la interfaz de usuario si ya se ha realizado para la sesión de cliente.

</dd> </dl>

Tenga en cuenta que para ejecutar una acción personalizada durante dos modos de ejecución diferentes, cree dos entradas en la [tabla CustomAction](customaction-table.md) . Por ejemplo, para tener una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) de C/C++ ( [tipo de acción personalizada 1](custom-action-type-1.md)) cuando el modo es MSIRUNMODE \_ programado y MSIRUNMODE \_ ROLLBACK, coloque dos entradas en la tabla CustomAction que llamen a la misma dll pero que tengan tipos numéricos diferentes. Incluya el código que llama a [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para determinar cuándo se debe ejecutar la acción personalizada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> </dl>

 

 



