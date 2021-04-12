---
title: Servicios básicos
description: Servicios básicos
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- e/s de archivos multimedia, servicios básicos
- e/s de archivos, servicios básicos
- entrada y salida (e/s), servicios básicos
- E/s (entrada y salida), servicios básicos
- e/s básicas
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420675"
---
# <a name="basic-services"></a>Servicios básicos

El uso de los servicios de e/s básicos es similar al uso de los servicios de e/s de archivos en tiempo de ejecución de la biblioteca en tiempo de ejecución de C. Los archivos se deben abrir antes de que se puedan leer o escribir. Después de leer o escribir, el archivo debe estar cerrado. También puede cambiar la ubicación de lectura o escritura actual dentro de un archivo abierto.

Antes de comenzar las operaciones de e/s en un archivo, debe abrir el archivo mediante la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Esta función devuelve un identificador de archivo de tipo **HMMIO**. Puede usar este identificador de archivo para identificar el archivo abierto al llamar a otras funciones de e/s de archivo.

> [!Note]  
> Un identificador de archivo **HMMIO** no es un identificador de archivo estándar. No use identificadores de archivo **HMMIO** con funciones de e/s de archivos en tiempo de ejecución de Win32 o C.

 

Cuando se usa [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para abrir un archivo, se usa una marca para especificar si se va a abrir para lectura, escritura o ambos. También puede especificar marcas que le permitan crear o eliminar un archivo. Use la función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para cerrar un archivo cuando haya terminado de leer o escribir en él.

Puede leer y escribir archivos mediante las funciones [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) y [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , respectivamente. La siguiente operación de lectura o escritura se produce en la posición del archivo actual o en el puntero de archivo de un archivo. La posición del archivo actual es avanzada cada vez que se lee o se escribe un archivo.

También puede cambiar la posición actual del archivo mediante la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) . Debe asegurarse de especificar una ubicación válida en un archivo. Si especifica una ubicación no válida, como más allá del final del archivo, es posible que **mmioSeek** no devuelva un error, pero se podrían producir errores en las operaciones de e/s posteriores.

Hay marcas que puede usar con la función **mmioOpen** para operaciones más allá de la e/s de archivos básica. Al especificar una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , por ejemplo, puede abrir archivos de memoria, especificar un procedimiento de e/s personalizado o proporcionar un búfer para la e/s almacenada en búfer.

 

 