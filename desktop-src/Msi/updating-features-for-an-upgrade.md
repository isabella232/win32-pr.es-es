---
description: El paquete de actualización de Windows Installer de ejemplo agrega nuevas características al producto original.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Actualizar características para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678141"
---
# <a name="updating-features-for-an-upgrade"></a>Actualizar características para una actualización

El paquete de actualización de ejemplo agrega tres características nuevas al producto original:

-   Baloncesto, una nueva característica secundaria de la característica deporte.
-   Opera, una nueva característica secundaria de la característica Arts.
-   Memorial, una nueva característica secundaria de la característica de la puerta.

Utilice el editor de base de datos para abrir MNP2001.msi y escriba los datos siguientes en la [tabla de características](feature-table.md).

[Tabla de características](feature-table.md)



| Característica    | Característica \_ principal | Title         | Descripción                | Pantalla | Nivel | Directorio\_ | Atributos |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Cultura       |                 | Cultura          | Arts Events en el Parque rojo.   | 18      | 3     | NOTEPADDIR  | 0          |
| Baloncesto   | Deporte           | Baloncesto      | Juegos de béisbol             | 17      | 3     | SPORTDIR    | 32         |
| Concierto    | Cultura            | Concierto       | Eventos de concierto en el Parque rojo | 19      | 3     | ARTSDIR     | 2          |
| Dance      | Cultura            | Dance         | Eventos de baile en el Parque rojo   | 21      | 3     | ARTSDIR     | 2          |
| Balón   | Deporte           | Balón      | Juegos de fútbol             | 13      | 3     | SPORTDIR    | 2          |
| Canaliza       |                 | Canaliza          | Admisiones del parque rojo      | 6       | 3     | NOTEPADDIR  | 0          |
| Ayuda       | Bloc de notas         | Ayuda          | Archivo de ayuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January    | Canaliza            | January       | Admisiones de enero         | 7       | 3     | MONDIR      | 2          |
| NewYears   | January         | Día de los años nuevos | Nuevas Admisiones del día de los años   | 9       | 3     | HOLDIR      | 2          |
| Bloc de notas    |                 | Bloc de notas       | Editor del Bloc de notas             | 1       | 3     | NOTEPADDIR  | 0          |
| Léame     | Bloc de notas         | Léame        | Archivo Léame                | 3       | 3     | NOTEPADDIR  | 0          |
| Deporte      |                 | Eventos deportivos  | Acontecimientos deportivos en el Parque rojo   | 12      | 3     | NOTEPADDIR  | 0          |
| Baloncesto | Deporte           | Baloncesto    | Juegos de baloncesto           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Cultura            | Opera         | Rendimiento de opera         | 23      | 3     | ARTSDIR     | 2          |
| Memorial   | Canaliza            | Día del recuerdo  | Admisiones del día del recuerdo    | 11      | 3     | HOLDIR      | 2          |



 

Use el editor de base de datos para abrir MNP2001.msi y escriba los datos siguientes en la [tabla FeatureComponents](featurecomponents-table.md)vacía.



| Característica\_  | Componente\_ |
|------------|-------------|
| Baloncesto   | Baloncesto    |
| Concierto    | Concierto     |
| Dance      | Dance       |
| Balón   | Balón    |
| Ayuda       | Ayuda        |
| January    | January     |
| NewYears   | NewYears    |
| Bloc de notas    | Bloc de notas     |
| Léame     | Bloc de notas     |
| Baloncesto | Baloncesto  |
| Opera      | Opera       |
| Memorial   | Memorial    |



 

[Continuar](updating-shortcuts-for-an-upgrade.md)

 

 



