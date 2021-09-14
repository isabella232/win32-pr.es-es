---
description: Describe un esquema de recopilación de dispersión para leer o escribir fragmentos no continuos de datos en una operación.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Leer o escribir en archivos mediante un esquema Scatter-Gather trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069863"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Leer o escribir en archivos mediante un esquema Scatter-Gather trabajo

Un esquema de recopilación de dispersión usa el sistema operativo para entregar en una operación varios fragmentos discretos de datos (como registros de base de datos) de un archivo para separar búferes no continuos en memoria. Un esquema de recopilación de dispersión también escribe los datos de búferes no continuos en una operación.

Una aplicación puede implementar un esquema de recopilación de dispersión mediante las funciones [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) y [**WriteFileGather.**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)

 

 



