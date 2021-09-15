---
description: Microsoft Installer permite a los usuarios instalar y quitar bloques de la funcionalidad de la aplicación a la que se hace referencia como Windows installer.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Especificar características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf7463b30247e921fb440ada1cd6f00f8e96a96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473935"
---
# <a name="specifying-features"></a>Especificar características

Microsoft Installer permite a los usuarios instalar y quitar bloques de funcionalidad de aplicación a los que se hace referencia [Windows características del instalador](windows-installer-features.md). En esta sección agregará información a la base de datos de instalación sobre las características disponibles para el Bloc de notas ejemplo. Para obtener más información, [vea Grupo de tablas principales](core-tables-group.md) y Componentes y [características.](components-and-features.md)

En Bloc de notas ejemplo se instalan características en una jerarquía de características primarias y secundarias. En la lista siguiente, se aplica sangría a las características secundarias en relación con su característica primaria. Las características deben mostrarse en este orden en el [control SelectionTree](selectiontree-control.md) de la interfaz de usuario (UI).

Bloc de notas

-   Léame
-   Ayuda

Puerta

-   January
    -   NewYears

Deporte

-   Béisbol
-   Fútbol

Arte

-   Concierto
-   Baile

Use un editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla [de características vacía](feature-table.md).



| Característica  | Elemento \_ primario de la característica | Título         | Descripción                | Mostrar | Nivel | Directorio\_ | Atributos |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arte     |                 | Arte          | Eventos de eventos en Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Béisbol | Deporte           | Béisbol      | Juegos de béisbol             | 17      | 3     | SPORTDIR    | 32         |
| Concierto  | Arte            | Concierto       | Eventos de un concierto en Red Park | 21      | 3     | NOCIONESDIR     | 2          |
| Baile    | Arte            | Baile         | Eventos de música en Red Park   | 23      | 3     | NOCIONESDIR     | 2          |
| Fútbol | Deporte           | Fútbol      | Partidos de fútbol             | 19      | 3     | SPORTDIR    | 2          |
| Puerta     |                 | Puerta          | Admisiones de Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Ayuda     | Bloc de notas         | Ayuda          | Archivo de ayuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January  | Puerta            | January       | Admisiones de enero         | 10      | 3     | MONDIR      | 2          |
| NewYears | January         | Día de los años nuevos | Admisiones de año nuevo   | 11      | 3     | HOLDIR      | 2          |
| Bloc de notas  |                 | Bloc de notas       | Bloc de notas Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Léame   | Bloc de notas         | Léame        | Archivo Léame                | 3       | 3     | NOTEPADDIR  | 0          |
| Deporte    |                 | Eventos deportivos  | Eventos deportivos en Red Park   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Continuar](specifying-feature-component-relationships.md)

 

 



