---
description: 'Para obtener un identificador para un volumen para su uso con operaciones de diario de cambio de número de secuencia de actualización (USN), llame a la función CreateFile con el parámetro lpFileName establecido en una cadena con el formato siguiente: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtener un identificador de volumen para las operaciones del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069893"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Obtener un identificador de volumen para las operaciones del diario de cambios

Para obtener un identificador para un volumen para su uso con operaciones de diario de cambio de número de secuencia de actualización (USN), llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el parámetro *lpFileName* establecido en una cadena con el formato siguiente: \\ \\ . \\ *X*:

Tenga en *cuenta que X* es la letra que identifica la unidad en la que aparece el volumen NTFS.

Si el volumen no tiene una letra de unidad, use la sintaxis descrita en [Asignación de nombres a un volumen.](naming-a-volume.md)

 

 



