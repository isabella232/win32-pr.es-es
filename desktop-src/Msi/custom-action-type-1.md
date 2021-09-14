---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar un tipo de acción personalizado 1 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo de acción personalizada 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158708"
---
# <a name="custom-action-type-1"></a>Tipo de acción personalizada 1

Esta acción personalizada llama a una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.

## <a name="source"></a>Source

El archivo DLL se genera a partir de una secuencia binaria temporal. El campo Source de la [tabla CustomAction contiene](customaction-table.md) una clave para [la tabla binaria](binary-table.md).

La columna Datos de la tabla Binaria contiene los datos de flujo. Se asigna una secuencia independiente para cada fila. Se pueden insertar nuevos datos binarios desde un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla. Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que luego se procesa en función del tipo de acción personalizada.

## <a name="type-value"></a>Valor de tipo

Incluya los siguientes bits de marca en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                          | Hexadecimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

## <a name="target"></a>Destino

Se llama al archivo DLL a través del punto de entrada denominado en el campo Target de la tabla [CustomAction](customaction-table.md), pasando un único argumento que es el identificador a la sesión de instalación actual. El nombre del punto de entrada especificado en la tabla debe coincidir con el que se exportó desde el archivo DLL. Tenga en cuenta que si la función de entrada no se especifica mediante . Archivo DEF o mediante una especificación del vinculador /EXPORT: , el nombre puede tener un carácter de subrayado inicial y un @4 sufijo "". La función llamada debe especificar la \_ \_ convención de llamada stdcall.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de devolución. Para obtener una descripción de las opciones y los valores, vea [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction para](customaction-table.md) especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en script. Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación. Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valores devueltos

Vea [Valores devueltos de acción personalizada.](custom-action-return-values.md)

## <a name="remarks"></a>Observaciones

Una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) requiere un identificador para la sesión de instalación. Si también se trata de una acción personalizada de ejecución aplazada, es posible que la sesión ya no exista durante la ejecución del script de instalación. Para obtener información sobre cómo una acción personalizada de este tipo puede obtener información de contexto, vea Obtener información de contexto para acciones personalizadas [de ejecución aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta denominada después de la tabla, usando la clave principal como nombre de archivo (columna Nombre de la tabla binaria), con una extensión predeterminada de ".ibd". El nombre debe usar el formato 8.3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos. El archivo de archivo persistente reemplaza los datos de secuencia por el nombre de archivo utilizado, de modo que los datos se puedan encontrar cuando se importe la tabla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> <dt>

[Bibliotecas de vínculos dinámicos](dynamic-link-libraries.md)
</dt> <dt>

[Obtener información de contexto para acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



