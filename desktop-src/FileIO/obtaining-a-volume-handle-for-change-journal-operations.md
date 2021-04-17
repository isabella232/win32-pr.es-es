---
description: 'Para obtener un identificador de un volumen para su uso con las operaciones del diario de cambios del número de secuencias actualizadas (USN), llame a la función CreateFile con el parámetro lpFileName establecido en una cadena de la siguiente forma: \\ \\ . \\ X1.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtención de un identificador de volumen para las operaciones del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669863"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Obtención de un identificador de volumen para las operaciones del diario de cambios

Para obtener un identificador de un volumen para su uso con las operaciones del diario de cambios del número de secuencias actualizadas (USN), llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el parámetro *lpFileName* establecido en una cadena de la siguiente forma: \\ \\ . \\ *X*:

Tenga en cuenta que *X* es la letra que identifica la unidad en la que aparece el volumen NTFS.

Si el volumen no tiene una letra de unidad, use la sintaxis descrita en [asignar un nombre a un volumen](naming-a-volume.md).

 

 



