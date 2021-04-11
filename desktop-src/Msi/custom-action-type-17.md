---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 17 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo de acción personalizada 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361399"
---
# <a name="custom-action-type-17"></a>Tipo de acción personalizada 17

Esta acción personalizada llama a una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.

## <a name="source"></a>Source

El archivo DLL se instala con la aplicación durante la sesión actual. El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de archivos](file-table.md). La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; por lo tanto, se debe llamar a esta acción personalizada después de instalar el archivo y antes de quitarlo.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Destino

Se llama a la DLL a través del punto de entrada denominado en el campo de destino de la [tabla CustomAction](customaction-table.md), pasando un solo argumento que es el identificador de la sesión de instalación actual. El nombre del punto de entrada especificado en la tabla debe coincidir con el exportado desde el archivo DLL. Tenga en cuenta que si la función de entrada no se especifica mediante un. Archivo DEF o una especificación/EXPORT: linker, el nombre puede tener un carácter de subrayado inicial y un @4 sufijo "". La función llamada debe especificar la \_ \_ Convención de llamada Stdcall.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos. Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Observaciones

Una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) requiere un identificador para la sesión de instalación. Si esta es también una acción personalizada de ejecución aplazada, es posible que la sesión ya no exista durante la ejecución del script de instalación. Para obtener información sobre cómo una acción personalizada de este tipo puede obtener información de contexto, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).

Las acciones personalizadas se ejecutan en un subproceso independiente y pueden tener acceso limitado al sistema. Las acciones personalizadas que se ejecutan de forma asincrónica bloquean el subproceso principal a la finalización de la secuencia actual o de la sesión de instalación hasta que devuelvan.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 17 (DLL), deben cumplir las siguientes restricciones de secuenciación:

-   La acción personalizada se debe secuenciar después de la [acción CostFinalize](costfinalize-action.md). Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el archivo DLL.
-   Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).
-   Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas no diferidas de este tipo se deben secuenciar después de la [acción InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> <dt>

[Acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculos dinámicos](dynamic-link-libraries.md)
</dt> </dl>

 

 



