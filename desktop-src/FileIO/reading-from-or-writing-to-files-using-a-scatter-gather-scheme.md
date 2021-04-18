---
description: Describe un esquema de dispersión y recopilación para leer o escribir fragmentos de datos no contiguos en una sola operación.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Leer o escribir en archivos mediante un esquema de Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668142"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Leer o escribir en archivos mediante un esquema de Scatter-Gather

Un esquema de dispersión y recopilación utiliza el sistema operativo para ofrecer en una operación varios fragmentos discretos de datos (como registros de base de datos) de un archivo a búferes independientes no contiguos en la memoria. Un esquema de dispersión y recopilación también escribe los datos de búferes no contiguos en una operación.

Una aplicación puede implementar un esquema de dispersión y recopilación mediante el uso de las funciones [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) y [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .

 

 



