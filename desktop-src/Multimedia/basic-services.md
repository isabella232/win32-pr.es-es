---
title: Servicios básicos
description: Servicios básicos
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- E/S de archivos multimedia, servicios básicos
- E/S de archivo, servicios básicos
- entrada y salida (E/S), servicios básicos
- E/S (entrada y salida), servicios básicos
- E/S básica
- Función mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062937"
---
# <a name="basic-services"></a>Servicios básicos

El uso de los servicios básicos de E/S es similar al uso de los servicios de E/S de archivos en tiempo de ejecución de la biblioteca en tiempo de ejecución de C. Los archivos deben abrirse antes de que se puedan leer o escribir. Después de leer o escribir, el archivo debe cerrarse. También puede cambiar la ubicación actual de lectura o escritura dentro de un archivo abierto.

Antes de comenzar las operaciones de E/S en un archivo, debe abrir el archivo mediante la [**función mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) Esta función devuelve un identificador de archivo de tipo **HMMIO**. Puede usar este identificador de archivo para identificar el archivo abierto al llamar a otras funciones de E/S de archivo.

> [!Note]  
> Un **identificador de archivo HMMIO** no es un identificador de archivo estándar. No use identificadores **de archivo HMMIO** con funciones de E/S de archivos en tiempo de ejecución win32 o C.

 

Cuando se usa [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para abrir un archivo, se usa una marca para especificar si lo está abriendo para lectura, escritura o ambos. También puede especificar marcas que le permitan crear o eliminar un archivo. Use la [**función mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para cerrar un archivo cuando haya terminado de leerlo o escribir en él.

Puede leer y escribir archivos mediante las funciones [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) y [**mmioWrite,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) respectivamente. La siguiente operación de lectura o escritura tiene lugar en la posición del archivo actual o en el puntero de archivo de un archivo. La posición actual del archivo se avanza cada vez que se lee o escribe un archivo.

También puede cambiar la posición actual del archivo mediante la [**función mmioSeek.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) Debe asegurarse de especificar una ubicación válida en un archivo. Si especifica una ubicación no válida, como después del final del archivo, es posible que **mmioSeek** no devuelva un error, pero las operaciones de E/S posteriores podrían producir un error.

Hay marcas que puede usar con la función **mmioOpen** para las operaciones más allá de la E/S básica de archivos. Al especificar una estructura [**MMIOINFO,**](/previous-versions//dd757322(v=vs.85)) por ejemplo, puede abrir archivos de memoria, especificar un procedimiento de E/S personalizado o proporcionar un búfer para E/S en búfer.

 

 