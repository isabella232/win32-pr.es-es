---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 1 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo de acción personalizada 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083355"
---
# <a name="custom-action-type-1"></a>Tipo de acción personalizada 1

Esta acción personalizada llama a una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.

## <a name="source"></a>Source

El archivo DLL se genera a partir de una secuencia binaria temporal. El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla binaria](binary-table.md).

La columna de datos de la tabla binaria contiene los datos de la secuencia. Se asigna una secuencia independiente para cada fila. Se pueden insertar nuevos datos binarios de un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla. Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que se procesa en función del tipo de acción personalizada.

## <a name="type-value"></a>Valor de tipo

Incluya los siguientes bits de marca en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

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

Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta con el nombre de la tabla, utilizando la clave principal como el nombre de archivo (columna Name de la tabla binaria), con una extensión predeterminada de ". ibd". El nombre debe usar el formato 8,3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos. El archivo de almacenamiento persistente reemplaza los datos de la secuencia por el nombre de archivo usado, de modo que los datos se pueden encontrar al importar la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculos dinámicos](dynamic-link-libraries.md)
</dt> <dt>

[Obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



