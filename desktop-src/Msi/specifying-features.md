---
description: El instalador de Microsoft permite a los usuarios instalar y quitar bloques de funcionalidad de la aplicación a la que se hace referencia como Windows Installer características.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Especificar características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf7463b30247e921fb440ada1cd6f00f8e96a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277157"
---
# <a name="specifying-features"></a>Especificar características

El instalador de Microsoft permite a los usuarios instalar y quitar bloques de funcionalidad de la aplicación a la que se hace referencia como [Windows Installer características](windows-installer-features.md). En esta sección, agregará información a la base de datos de instalación sobre las características disponibles para el ejemplo del Bloc de notas. Para obtener más información, vea [grupo de tablas básicas](core-tables-group.md) y [componentes y características](components-and-features.md).

El ejemplo de Bloc de notas instala características en una jerarquía de características principales y secundarias. En la siguiente lista, se aplica sangría a las características secundarias en relación con su característica primaria. Las características deben mostrarse en este orden en el [control SelectionTree](selectiontree-control.md) de la interfaz de usuario (UI).

Bloc de notas

-   Léame
-   Ayuda

Canaliza

-   January
    -   NewYears

Deporte

-   Baloncesto
-   Balón

Cultura

-   Concierto
-   Dance

Use un editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la [tabla de características](feature-table.md)vacía.



| Característica  | Característica \_ principal | Title         | Descripción                | Pantalla | Nivel | Directorio\_ | Atributos |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Cultura     |                 | Cultura          | Arts Events en el Parque rojo.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baloncesto | Deporte           | Baloncesto      | Juegos de béisbol             | 17      | 3     | SPORTDIR    | 32         |
| Concierto  | Cultura            | Concierto       | Eventos de concierto en el Parque rojo | 21      | 3     | ARTSDIR     | 2          |
| Dance    | Cultura            | Dance         | Eventos de baile en el Parque rojo   | 23      | 3     | ARTSDIR     | 2          |
| Balón | Deporte           | Balón      | Juegos de fútbol             | 19      | 3     | SPORTDIR    | 2          |
| Canaliza     |                 | Canaliza          | Admisiones del parque rojo      | 6       | 3     | NOTEPADDIR  | 0          |
| Ayuda     | Bloc de notas         | Ayuda          | Archivo de ayuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January  | Canaliza            | January       | Admisiones de enero         | 10      | 3     | MONDIR      | 2          |
| NewYears | January         | Día de los años nuevos | Nuevas Admisiones del día de los años   | 11      | 3     | HOLDIR      | 2          |
| Bloc de notas  |                 | Bloc de notas       | Editor del Bloc de notas             | 1       | 3     | NOTEPADDIR  | 0          |
| Léame   | Bloc de notas         | Léame        | Archivo Léame                | 3       | 3     | NOTEPADDIR  | 0          |
| Deporte    |                 | Eventos deportivos  | Acontecimientos deportivos en el Parque rojo   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Continuar](specifying-feature-component-relationships.md)

 

 



