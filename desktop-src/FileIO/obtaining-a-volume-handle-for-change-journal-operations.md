---
description: 'Para obtener un identificador para un volumen para su uso con operaciones de diario de cambio de número de secuencia de actualización (USN), llame a la función CreateFile con el parámetro lpFileName establecido en una cadena con el formato siguiente: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtener un identificador de volumen para las operaciones del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a7e8090e419df2034d1e1e1726dd74cf2b2915f6976a042a47c73544fa6b38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683485"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Obtener un identificador de volumen para las operaciones del diario de cambios

Para obtener un identificador para un volumen para su uso con operaciones de diario de cambio de número de secuencia de actualización (USN), llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el parámetro *lpFileName* establecido en una cadena con el formato siguiente: \\ \\ . \\ *X*:

Tenga en *cuenta que X* es la letra que identifica la unidad en la que aparece el volumen NTFS.

Si el volumen no tiene una letra de unidad, use la sintaxis descrita en [Asignación de nombres a un volumen.](naming-a-volume.md)

 

 



