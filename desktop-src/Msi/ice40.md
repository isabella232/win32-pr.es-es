---
description: ICE40 realiza una validación miscelánea.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077c44154413d9aa9e75b1c13fe2f2f80ccb52fee6459888c7bc9678ea0e935f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528435"
---
# <a name="ice40"></a>ICE40

ICE40 realiza una validación miscelánea.

## <a name="result"></a>Resultado

ICE40 publica advertencias sobre lo siguiente:

-   Se ha invalidado la propiedad [**REINSTALLMODE.**](reinstallmode.md)
-   La [tabla RemoveIniFile](removeinifile-table.md) tiene una entrada Delete Tag sin ningún valor.
-   Al .msi falta la tabla [Error](error-table.md) y la propiedad [**Resumen**](page-count-summary.md) de recuento de páginas es menor o igual que 100. Esta advertencia de ICE está obsoleta porque Windows instalador no requiere que el paquete tenga una tabla de errores. Los mensajes de error se pueden recuperar mediante Msimsg.dll.

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

ICE40 notificaría los errores siguientes.



| Error ICE40                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) se define en la tabla Property. Esto puede causar dificultades. | La [**definición de la**](reinstallmode.md) propiedad REINSTALLMODE .msi archivo puede provocar un comportamiento inesperado. Para corregir este error, no defina esta propiedad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La entrada RemoveIniFile Remove1 debe tener un valor, porque la acción es "Delete Tag" (4).                | Hay una acción Eliminar etiqueta en en la columna RemoveIniFile de la tabla [RemoveIniFile](removeinifile-table.md) sin especificar una etiqueta para eliminar en la columna Valor.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Falta la tabla de errores. Solo se generarán mensajes de error numéricos.                              | Esta advertencia de ICE está obsoleta porque Windows instalador no requiere que el paquete tenga una [tabla de errores](error-table.md). Los mensajes de error se pueden recuperar mediante Msimsg.dll.<br/> Esta advertencia significa que el archivo .msi falta la tabla [Error](error-table.md) y la propiedad [**Resumen**](page-count-summary.md) del recuento de páginas es menor o igual que 100. <br/> Para corregir este error, use una versión actual del instalador de Windows o agregue una tabla error al paquete de instalación y cree plantillas de formato en la columna Mensaje para los mensajes de error.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




