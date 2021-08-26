---
description: Describe un esquema de dispersión y recopilación para leer o escribir fragmentos de datos no continuos en una sola operación.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lectura o escritura en archivos mediante un esquema Scatter-Gather datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc8a7ee9fcae2a54ac31c51a7c038e3d9442a6ccded2fc7dab916c7a6165a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914485"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lectura o escritura en archivos mediante un esquema Scatter-Gather datos

Un esquema de recopilación de dispersión usa el sistema operativo para entregar en una operación varios fragmentos discretos de datos (como registros de base de datos) de un archivo a búferes independientes y no continuos en memoria. Un esquema de dispersión y recopilación también escribe los datos de búferes no continuos en una operación.

Una aplicación puede implementar un esquema de recopilación de dispersión mediante las funciones [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) y [**WriteFileGather.**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)

 

 



