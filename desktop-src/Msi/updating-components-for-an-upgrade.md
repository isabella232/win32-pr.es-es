---
description: Por diseño, los usuarios del producto MNP2000 ficticio nunca deben usar archivos actualizados como Baseba01.txt.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Actualización de componentes para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 920bc955d3d3615941ef03ec885ca8871f79dc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002691"
---
# <a name="updating-components-for-an-upgrade"></a>Actualización de componentes para una actualización

Por diseño, los usuarios del producto MNP2000 ficticio nunca deben usar archivos actualizados como Baseba01.txt. Por lo tanto, los archivos actualizados son por definición incompatibles con el producto original y los componentes de Windows Installer, como el béisbol, los que contienen estos archivos deben tener asignados nuevos códigos de componente. Los nuevos archivos, como Opera01.txt, se incluyen como parte de un componente nuevo con un código de componente único. Dado que el producto y la actualización originales usan el mismo componente de Bloc de notas, el código de componente de este componente no cambia. Para obtener más información sobre cuándo se debe cambiar el código del componente, vea [cambiar el código del componente](changing-the-component-code.md).

Use Orca u otro editor de bases de datos para especificar los datos siguientes en la [tabla de componentes](component-table.md) de MNP2001.msi. No reutilice los GUID que se muestran a continuación en la columna ComponentId en el ejemplo.

[Tabla de componentes](component-table.md)



| Componente  | ComponentId                            | Directorio\_ | Atributos | Condición | Rutas      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Baloncesto   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| Baloncesto | {E1AAB6B0-FEC6-4F18-B765-3B05A81CEACB} | SPORTDIR    | 2          |           | Basket01.txt |
| Concierto    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | ARTSDIR     | 2          |           | Concer01.txt |
| Dance      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | ARTSDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | ARTSDIR     | 2          |           | Opera01.txt  |
| Balón   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Ayuda       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | MONDIR      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| Memorial   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| Bloc de notas    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[Continuar](updating-features-for-an-upgrade.md)

 

 



