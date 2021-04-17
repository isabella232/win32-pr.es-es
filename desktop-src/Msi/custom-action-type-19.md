---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 19 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo de acción personalizada 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670002"
---
# <a name="custom-action-type-19"></a>Tipo de acción personalizada 19

Esta acción personalizada muestra un mensaje de error especificado, devuelve un error y, a continuación, finaliza la instalación. El mensaje de error mostrado se puede proporcionar como una cadena o como un índice en la [tabla de errores](error-table.md).

## <a name="source"></a>Source

Deje en blanco la columna de origen de la [tabla CustomAction](customaction-table.md) .

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la tabla CustomAction para especificar el tipo numérico básico.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Destino

La columna de destino de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con el formato de la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numérico). Los parámetros que se van a reemplazar se incluyen entre corchetes, \[ ... \] y pueden ser propiedades, variables de entorno (% Prefix), rutas de acceso de archivo ( \# prefijo) o rutas de acceso de directorio de componentes ($ Prefix). Si después de dar formato a la cadena se evalúa como un entero, ese entero se utiliza como índice en la [tabla de errores](error-table.md) para recuperar el mensaje que se va a mostrar. Si después de dar formato a la cadena contiene caracteres no numéricos, la propia cadena se muestra como el mensaje.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

La acción personalizada no usa ninguna opción.

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

La acción personalizada no usa ninguna opción.

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

La acción personalizada no usa ninguna opción.

## <a name="return-values"></a>Valores devueltos

Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Observaciones

Por ejemplo, las acciones personalizadas CAError1, CAError2, CAError3 y CAError4 devuelven estos mensajes.

[Tabla CustomAction](customaction-table.md)



| Acción   | Tipo | Source | Destino                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Error de instalación debido a Error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Tabla de propiedades](property-table.md)



| Propiedad | Value                                 |
|----------|---------------------------------------|
| Prop1    | "Error de instalación debido a Error1". |
| Prop2    | "25100"                               |



 

[Tabla de errores](error-table.md)



| Código  | Message                             |
|-------|-------------------------------------|
| 25000 | Error de instalación debido a error3. |
| 25100 | Error de instalación debido a Error4. |



 

Estas acciones personalizadas devuelven los siguientes mensajes de error:



| Acción personalizada | Cadena de mensaje devuelta             |
|---------------|-------------------------------------|
| CAError1      | Error de instalación debido a Error1. |
| CAError2      | Error de instalación debido a Error2. |
| CAError3      | Error de instalación debido a error3. |
| CAError4      | Error de instalación debido a Error4. |



 

Tenga en cuenta que, dado que el orden de evaluación de las condiciones de inicio no se puede garantizar mediante la creación de la [tabla LaunchCondition](launchcondition-table.md), debe usar las acciones personalizadas del tipo de acción personalizada 19 en la instalación para evaluar las condiciones en un orden específico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> </dl>

 

 



