---
description: Dado que la actualización actualiza los archivos usados por la aplicación, debe modificar la tabla de archivos de la base de datos.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Actualizar archivos y atributos de archivo para una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c1d749a61376d38e8c7793ba5766dd63133bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653105"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Actualizar archivos y atributos de archivo para una actualización

Dado que la actualización actualiza los archivos usados por la aplicación, debe modificar la [tabla de archivos](file-table.md) de la base de datos. Use el editor de bases de datos orca que se proporciona con el SDK u otro editor para abrir MNP2001.msi y escriba los datos siguientes en la [tabla de archivos](file-table.md).

[Tabla de archivos](file-table.md)



| Archivo         | Componente\_ | FileName     | FileSize | Versión | Idioma | Atributos | Secuencia |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Baloncesto    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | Concierto     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | Dance       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | Balón    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | Baloncesto  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ayuda        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | January     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | NewYears    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | Memorial    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloc de notas     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continuar](updating-components-for-an-upgrade.md)

 

 



