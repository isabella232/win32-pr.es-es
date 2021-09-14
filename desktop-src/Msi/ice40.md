---
description: ICE40 realiza una validación miscelánea.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074611"
---
# <a name="ice40"></a>ICE40

ICE40 realiza una validación miscelánea.

## <a name="result"></a>Resultado

ICE40 publica advertencias sobre lo siguiente:

-   Se [**ha invalidado**](reinstallmode.md) la propiedad REINSTALLMODE.
-   La [tabla RemoveIniFile](removeinifile-table.md) tiene una entrada Delete Tag sin ningún valor.
-   El .msi falta la [tabla Error](error-table.md) y la propiedad [**Resumen**](page-count-summary.md) de recuento de páginas es menor o igual que 100. Esta advertencia de ICE está obsoleta porque Windows Installer no requiere que el paquete tenga una tabla de errores. Los mensajes de error se pueden recuperar mediante Msimsg.dll.

## <a name="example"></a>Ejemplo

[Tabla de propiedades](property-table.md)



| Propiedad.                               | Value |
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
| [**REINSTALLMODE**](reinstallmode.md) se define en la tabla Property. Esto puede causar dificultades. | Definir la [**propiedad REINSTALLMODE**](reinstallmode.md) en .msi archivo puede provocar un comportamiento inesperado. Para corregir este error, no defina esta propiedad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La entrada RemoveIniFile Remove1 debe tener un valor, porque la acción es "Delete Tag" (4).                | Hay una acción Eliminar etiqueta en en la columna RemoveIniFile de la [tabla RemoveIniFile](removeinifile-table.md) sin especificar una etiqueta para eliminar en la columna Valor.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Falta la tabla de errores. Solo se generarán mensajes de error numéricos.                              | Esta advertencia de ICE está obsoleta porque Windows Installer no requiere que el paquete tenga una [tabla de errores](error-table.md). Los mensajes de error se pueden recuperar mediante Msimsg.dll.<br/> Esta advertencia significa que el archivo .msi falta la tabla [Error](error-table.md) y la propiedad [**Resumen**](page-count-summary.md) del recuento de páginas es menor o igual que 100. <br/> Para corregir este error, use una versión actual del instalador de Windows o agregue una tabla Error al paquete de instalación y cree plantillas de formato en la columna Mensaje para los mensajes de error.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




