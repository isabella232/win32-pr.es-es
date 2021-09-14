---
description: El ejemplo Windows paquete de actualización del instalador agrega nuevas características al producto original.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Actualizar características para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375202"
---
# <a name="updating-features-for-an-upgrade"></a>Actualizar características para una actualización

El paquete de actualización de ejemplo agrega tres nuevas características al producto original:

-   El deporte, una nueva característica secundaria de la característica Deport.
-   Opera, una nueva característica secundaria de la característica Desfila.
-   Así, una nueva característica secundaria de la característica Puerta.

Use el editor de bases de datos para MNP2001.msi y escriba los datos siguientes en la [tabla Característica](feature-table.md).

[Tabla de características](feature-table.md)



| Característica    | Elemento \_ primario de la característica | Título         | Descripción                | Mostrar | Nivel | Directorio\_ | Atributos |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arte       |                 | Arte          | Eventos de eventos en Red Park.   | 18      | 3     | NOTEPADDIR  | 0          |
| Béisbol   | Deporte           | Béisbol      | Juegos de béisbol             | 17      | 3     | SPORTDIR    | 32         |
| Concierto    | Arte            | Concierto       | Eventos de un concierto en Red Park | 19      | 3     | NOCIONESDIR     | 2          |
| Baile      | Arte            | Baile         | Eventos de música en Red Park   | 21      | 3     | NOCIONESDIR     | 2          |
| Fútbol   | Deporte           | Fútbol      | Partidos de fútbol             | 13      | 3     | SPORTDIR    | 2          |
| Puerta       |                 | Puerta          | Admisiones de Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Ayuda       | Bloc de notas         | Ayuda          | Archivo de ayuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January    | Puerta            | January       | Admisiones de enero         | 7       | 3     | MONDIR      | 2          |
| NewYears   | January         | Día de los años nuevos | Admisiones de año nuevo   | 9       | 3     | HOLDIR      | 2          |
| Bloc de notas    |                 | Bloc de notas       | Bloc de notas Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Léame     | Bloc de notas         | Léame        | Archivo Léame                | 3       | 3     | NOTEPADDIR  | 0          |
| Deporte      |                 | Eventos deportivos  | Eventos deportivos en Red Park   | 12      | 3     | NOTEPADDIR  | 0          |
| Baloncesto | Deporte           | Baloncesto    | Juegos de clubes           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Arte            | Opera         | Representaciones de opera         | 23      | 3     | NOCIONESDIR     | 2          |
| Memorial   | Puerta            | Día de los caídos  | Admisiones del día de la noche    | 11      | 3     | HOLDIR      | 2          |



 

Use el editor de bases de datos para MNP2001.msi y escriba los datos siguientes en la tabla [FeatureComponents vacía.](featurecomponents-table.md)



| Característica\_  | Componente\_ |
|------------|-------------|
| Béisbol   | Béisbol    |
| Concierto    | Concierto     |
| Baile      | Baile       |
| Fútbol   | Fútbol    |
| Ayuda       | Ayuda        |
| January    | January     |
| NewYears   | NewYears    |
| Bloc de notas    | Bloc de notas     |
| Léame     | Bloc de notas     |
| Baloncesto | Baloncesto  |
| Opera      | Opera       |
| Memorial   | Memorial    |



 

[Continuar](updating-shortcuts-for-an-upgrade.md)

 

 



