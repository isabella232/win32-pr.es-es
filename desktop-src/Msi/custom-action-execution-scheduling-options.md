---
description: Dado que una acción personalizada se puede programar en la interfaz de usuario y ejecutar tablas de secuencia, y se puede ejecutar en el proceso de servicio o cliente, una acción personalizada puede ejecutarse varias veces.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opciones de programación de ejecución de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158727"
---
# <a name="custom-action-execution-scheduling-options"></a>Opciones de programación de ejecución de acciones personalizadas

Dado que una acción personalizada se puede programar en la interfaz de usuario y ejecutar tablas de secuencia, y se puede ejecutar en el proceso de servicio o cliente, una acción personalizada puede ejecutarse varias veces.

Tenga en cuenta que el instalador:

-   Ejecuta acciones en una tabla de secuencia inmediatamente de forma predeterminada.
-   No ejecuta una acción si el campo de expresión condicional de la tabla de secuencia se evalúa como False.
-   Procesa la tabla de secuencia de interfaz de usuario en el proceso de cliente si el nivel de interfaz del usuario interno está establecido en el modo de interfaz de usuario completo (vea [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obtener una descripción de los niveles de interfaz de usuario).
-   Es un servicio registrado de forma predeterminada cuando se usa Windows 2000 y, en este caso, la tabla de secuencia de ejecución se procesa en el servicio del instalador.

Puede usar las siguientes marcas de opción para controlar la ejecución inmediata de acciones personalizadas. Para establecer una opción, agregue el valor de esta tabla al valor del campo Tipo de la [tabla CustomAction](customaction-table.md). No se debe usar ninguna de las marcas siguientes con acciones [personalizadas de ejecución aplazada.](deferred-execution-custom-actions.md)

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>(valor predeterminado)
</dt> <dd>

Hexadecimal: 0x00000000

Decimal: 0

Ejecute siempre. La acción se puede ejecutar dos veces si está presente en ambas tablas de secuencia.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Hexadecimal: 0x00000100

Decimal: 256

Ejecute no más de una vez si está presente en ambas tablas de secuencia. Siempre omite la acción en la secuencia de ejecución si se ha ejecutado la secuencia de interfaz de usuario. No hay ningún efecto en la secuencia de interfaz de usuario. No es necesario que la acción esté presente ni se ejecute en la secuencia de interfaz de usuario que se omitirá en la secuencia de ejecución. No se ve afectado por el registro del servicio de instalación.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Hexadecimal: 0x00000200

Decimal: 512

Ejecute una vez por proceso si se encuentra en ambas tablas de secuencia. Omite la acción en la secuencia de ejecución si la secuencia de interfaz de usuario se ha ejecutado en el mismo proceso, por ejemplo, ambas se ejecutan en el proceso de cliente. Se usa para evitar que las acciones que modifican el estado de sesión, como los datos de propiedad y base de datos, se ejecuten dos veces.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Hexadecimal: 0x00000300

Decimal: 768

Ejecute solo si se ejecuta en el cliente después de que se haya ejecutado la secuencia de interfaz de usuario. La acción solo se ejecuta si la secuencia de ejecución se ejecuta en la secuencia de interfaz de usuario siguiente del cliente. Se puede usar para proporcionar lógica o , o para suprimir el procesamiento relacionado con la interfaz de usuario si ya se ha realizado para la sesión de cliente.

</dd> </dl>

Tenga en cuenta que para ejecutar una acción personalizada durante dos modos de ejecución diferentes, cree dos entradas en la [tabla CustomAction](customaction-table.md) . Por ejemplo, para tener una acción personalizada que llame a una biblioteca de vínculos dinámicos (DLL) de C/C++ (tipo de acción personalizada [1),](custom-action-type-1.md)tanto cuando el modo es MSIRUNMODE SCHEDULED como \_ MSIRUNMODE ROLLBACK, coloque dos entradas en la tabla CustomAction que llaman al mismo archivo DLL pero que tienen tipos numéricos \_ diferentes. Incluya código que llame [**a MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para determinar cuándo ejecutar qué acción personalizada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> </dl>

 

 



