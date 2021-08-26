---
description: Por diseño, los usuarios del producto ficticio MNP2000 nunca deben usar archivos actualizados, como Baseba01.txt.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Actualizar componentes para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e725653acc7aadbeb3710d3cd6b1ee6dc2971e51d3583f2be279ddfed008d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039245"
---
# <a name="updating-components-for-an-upgrade"></a>Actualizar componentes para una actualización

Por diseño, los usuarios del producto ficticio MNP2000 nunca deben usar archivos actualizados, como Baseba01.txt. Por lo tanto, los archivos actualizados no son compatibles por definición con el producto original y los componentes del instalador de Windows, como Baseball, que contiene estos archivos deben tener asignados nuevos códigos de componente. Los nuevos archivos, como Opera01.txt, se presentan como parte de un nuevo componente con un código de componente único. Dado que el producto y la actualización originales usan el mismo Bloc de notas componente, el código de componente de este componente no se modifica. Para obtener más información sobre cuándo se debe cambiar el código de componente, vea [Cambiar el código de componente](changing-the-component-code.md).

Use Orca u otro editor de bases de datos para escribir los datos siguientes en la [tabla Component](component-table.md) de MNP2001.msi. No reutilice los GUID que se muestran a continuación en la columna ComponentId del ejemplo.

[Tabla de componentes](component-table.md)



| Componente  | Componentid                            | Directorio\_ | Atributos | Condición | Ruta de acceso de clave      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Béisbol   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| Baloncesto | {E1AAB6B0-FEC6-4F18-B765-3B05A81CBCB} | SPORTDIR    | 2          |           | Basket01.txt |
| Concierto    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | NOCIONESDIR     | 2          |           | Concer01.txt |
| Baile      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | NOCIONESDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | NOCIONESDIR     | 2          |           | Opera01.txt  |
| Fútbol   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Ayuda       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | MONDIR      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| Memorial   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| Bloc de notas    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[Continuar](updating-features-for-an-upgrade.md)

 

 



