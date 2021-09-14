---
description: Los desarrolladores de Windows Installer pueden optar por usar un tipo de acción personalizada 17 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo de acción personalizada 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158707"
---
# <a name="custom-action-type-17"></a>Tipo de acción personalizada 17

Esta acción personalizada llama a una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.

## <a name="source"></a>Source

El archivo DLL se instala con la aplicación durante la sesión actual. El campo Source de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla File](file-table.md). La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; Por lo tanto, se debe llamar a esta acción personalizada una vez instalado ese archivo y antes de quitarlo.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Destino

Se llama al archivo DLL a través del punto de entrada denominado en el campo Destino de la tabla [CustomAction](customaction-table.md), pasando un único argumento que es el identificador de la sesión de instalación actual. El nombre del punto de entrada especificado en la tabla debe coincidir con el que se exportó desde el archivo DLL. Tenga en cuenta que si la función de entrada no se especifica mediante . El archivo DEF o mediante una especificación /EXPORT: del vinculador, el nombre puede tener un carácter de subrayado inicial y un sufijo @4 "". La función llamada debe especificar la \_ \_ convención de llamada stdcall.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Opciones de programación de ejecución de acciones personalizadas.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Vea [Valores devueltos de acciones personalizadas.](custom-action-return-values.md)

## <a name="remarks"></a>Observaciones

Una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) requiere un identificador para la sesión de instalación. Si también se trata de una acción personalizada de ejecución aplazada, es posible que la sesión ya no exista durante la ejecución del script de instalación. Para obtener información sobre cómo una acción personalizada de este tipo puede obtener información de contexto, vea Obtener información de contexto para acciones personalizadas [de ejecución aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Las acciones personalizadas se ejecutan en un subproceso independiente y pueden tener acceso limitado al sistema. Las acciones personalizadas que se ejecutan de forma asincrónica bloquean el subproceso principal al finalizar la secuencia actual o la sesión de instalación hasta que se devuelven.

Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como Custom Action Type 17 (DLL), deben cumplir las siguientes restricciones de secuenciación:

-   La acción personalizada debe secuenciarse después de [la acción CostFinalize](costfinalize-action.md). Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el archivo DLL.
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).
-   Si el archivo de origen aún no está instalado en el equipo, las acciones personalizadas no diferidas de este tipo deben secuenciarse después de [la acción InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> <dt>

[Acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculos dinámicos](dynamic-link-libraries.md)
</dt> </dl>

 

 



