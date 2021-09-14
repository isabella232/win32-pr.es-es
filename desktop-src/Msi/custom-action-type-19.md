---
description: Los desarrolladores Windows paquetes del instalador pueden optar por usar una acción personalizada de tipo 19 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo de acción personalizada 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158703"
---
# <a name="custom-action-type-19"></a>Tipo de acción personalizada 19

Esta acción personalizada muestra un mensaje de error especificado, devuelve un error y, a continuación, finaliza la instalación. El mensaje de error que se muestra se puede proporcionar como una cadena o como un índice en la [tabla Error](error-table.md).

## <a name="source"></a>Source

Deje la columna Origen de la [tabla CustomAction en](customaction-table.md) blanco.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Tipo de la tabla CustomAction para especificar el tipo numérico básico.



| Constantes                                                               | Hexadecimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Destino

La columna Target de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con formato con la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numérico). Los parámetros que se van a reemplazar se incluyen entre corchetes, ... y pueden ser propiedades, variables de entorno (% de prefijo), rutas de acceso de archivo (prefijo) o rutas de acceso de directorio de \[ \] componentes \# (prefijo $). Si después de dar formato a la cadena se evalúa como un entero, ese entero se usa como índice en la [tabla Error](error-table.md) para recuperar el mensaje que se va a mostrar. Si después de dar formato a la cadena contiene caracteres no numéricos, la propia cadena se muestra como mensaje.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

La acción personalizada no usa ninguna opción.

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

La acción personalizada no usa ninguna opción.

## <a name="in-script-execution-options"></a>In-Script de ejecución

La acción personalizada no usa ninguna opción.

## <a name="return-values"></a>Valores devueltos

Vea [Valores devueltos de acción personalizada.](custom-action-return-values.md)

## <a name="remarks"></a>Observaciones

Por ejemplo, las acciones personalizadas CAError1, CAError2, CAError3 y CAError4 devuelven estos mensajes.

[CustomAction (tabla)](customaction-table.md)



| Acción   | Tipo | Source | Destino                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Error de instalación debido a Error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Tabla de propiedades](property-table.md)



| Propiedad. | Value                                 |
|----------|---------------------------------------|
| Prop1    | "Error de instalación debido a Error1". |
| Prop2    | "25100"                               |



 

[Tabla de errores](error-table.md)



| Código  | Message                             |
|-------|-------------------------------------|
| 25000 | Error de instalación debido a Error3. |
| 25100 | Error de instalación debido a Error4. |



 

Estas acciones personalizadas devuelven los siguientes mensajes de error:



| Acción personalizada | Cadena de mensaje devuelta             |
|---------------|-------------------------------------|
| CAError1      | Error de instalación debido a Error1. |
| CAError2      | Error de instalación debido a Error2. |
| CAError3      | Error de instalación debido a Error3. |
| CAError4      | Error de instalación debido a Error4. |



 

Tenga en cuenta que, dado que no se puede garantizar el orden de evaluación de las condiciones de inicio mediante la creación de la tabla [LaunchCondition](launchcondition-table.md), debe usar acciones personalizadas de tipo de acción personalizada 19 en la instalación para evaluar las condiciones en un orden específico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> </dl>

 

 



