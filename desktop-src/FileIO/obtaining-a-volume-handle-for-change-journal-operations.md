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
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a><span data-ttu-id="8bf38-103">Obtención de un identificador de volumen para las operaciones del diario de cambios</span><span class="sxs-lookup"><span data-stu-id="8bf38-103">Obtaining a Volume Handle for Change Journal Operations</span></span>

<span data-ttu-id="8bf38-104">Para obtener un identificador de un volumen para su uso con las operaciones del diario de cambios del número de secuencias actualizadas (USN), llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el parámetro *lpFileName* establecido en una cadena de la siguiente forma: \\ \\ . \\ *X*:</span><span class="sxs-lookup"><span data-stu-id="8bf38-104">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*:</span></span>

<span data-ttu-id="8bf38-105">Tenga en cuenta que *X* es la letra que identifica la unidad en la que aparece el volumen NTFS.</span><span class="sxs-lookup"><span data-stu-id="8bf38-105">Note that *X* is the letter that identifies the drive on which the NTFS volume appears.</span></span>

<span data-ttu-id="8bf38-106">Si el volumen no tiene una letra de unidad, use la sintaxis descrita en [asignar un nombre a un volumen](naming-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-106">If the volume does not have a drive letter, use the syntax described in [Naming a Volume](naming-a-volume.md).</span></span>

 

 



