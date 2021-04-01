---
description: ICE36 valida que cada icono de la tabla de iconos aparece al menos una vez en la propiedad ARPPRODUCTICON o en las tablas Class, ProgId o Shortcut.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082926"
---
# <a name="ice36"></a>ICE36

ICE36 valida que cada icono de la tabla de iconos aparece al menos una vez en la propiedad [**ARPPRODUCTICON**](arpproducticon.md) o en las tablas [Class](class-table.md), [ProgID](progid-table.md)o [Shortcut](shortcut-table.md) .

Durante el anuncio, el instalador instala todos los iconos que aparecen en la [tabla de iconos](icon-table.md) en el equipo del usuario. Tener iconos sin usar en la tabla de iconos no impide que la instalación se ejecute, pero sí aumenta innecesariamente el tamaño del archivo. msi y la hora y el espacio necesarios para anunciar una característica.

Si no se hace referencia a un icono en la propiedad o la tabla y no se proporciona ninguna interfaz de usuario para crear una referencia en tiempo de ejecución, debe quitar el icono para lograr un mejor rendimiento.

## <a name="result"></a>Resultado

ICE36 envía un mensaje si hay un icono en la tabla de iconos al que no se hace referencia en las tablas [Class](class-table.md), [ProgID](progid-table.md)o [Shortcut](shortcut-table.md) y si no se proporciona ninguna interfaz de usuario para crear dicha referencia en tiempo de ejecución.

## <a name="example"></a>Ejemplo

ICE36 notifica el siguiente error para el ejemplo que se muestra.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Tabla de iconos](icon-table.md) (parcial)



| Nombre  | Datos     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Control2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[Tabla ProgID](progid-table.md) (parcial)



| ProgID    |
|-----------|
| Property1 |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Icono\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



