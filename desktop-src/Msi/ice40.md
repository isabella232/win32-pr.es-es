---
description: ICE40 realiza una validación diversa.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156717"
---
# <a name="ice40"></a>ICE40

ICE40 realiza una validación diversa.

## <a name="result"></a>Resultado

ICE40 expone advertencias en lo siguiente:

-   Se ha invalidado la propiedad [**REINSTALLMODE**](reinstallmode.md) .
-   La [tabla RemoveIniFile](removeinifile-table.md) tiene una entrada de etiqueta DELETE sin ningún valor.
-   Falta la [tabla de errores](error-table.md) en el archivo. msi y la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) es menor o igual que 100. Esta advertencia de ICE está obsoleta porque Windows Installer no requiere que el paquete tenga una tabla de errores. Los mensajes de error se pueden recuperar mediante Msimsg.dll.

## <a name="example"></a>Ejemplo

[Tabla de propiedades](property-table.md)



| Propiedad                               | Value |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | A     |



 

[Tabla RemoveIniFile](removeinifile-table.md)



| RemoveIniFile                          | Acción | Value |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>Results

ICE40 notificaría los siguientes errores.



| Error ICE40                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) se define en la tabla de propiedades. Esto puede producir dificultades. | La definición de la propiedad [**REINSTALLMODE**](reinstallmode.md) en el archivo. msi puede provocar un comportamiento inesperado. Para corregir este error, no defina esta propiedad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La entrada RemoveIniFile Remove1 debe tener un valor, porque la acción es "eliminar etiqueta" (4).                | Hay una acción de eliminación de etiqueta en la columna RemoveIniFile de la [tabla RemoveIniFile](removeinifile-table.md) sin especificar la etiqueta que se va a eliminar en la columna valor.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Falta la tabla de errores. Solo se generarán mensajes de error numéricos.                              | Esta advertencia de ICE está obsoleta porque Windows Installer no requiere que el paquete tenga una [tabla de errores](error-table.md). Los mensajes de error se pueden recuperar mediante Msimsg.dll.<br/> Esta ADVERTENCIA significa que en el archivo. msi falta la [tabla de errores](error-table.md) y la propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) es menor o igual que 100. <br/> Para corregir este error, use una versión actual del Windows Installer o agregue una tabla de errores al paquete de instalación y plantillas de formato de autor en la columna mensaje para los mensajes de error.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




