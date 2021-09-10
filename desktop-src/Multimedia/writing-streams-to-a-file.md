---
title: Escribir Secuencias en un archivo
description: Escribir Secuencias en un archivo
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- Función AVIFileCreateStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372482"
---
# <a name="writing-streams-to-a-file"></a>Escribir Secuencias en un archivo

También puede crear un archivo que contenga flujos de datos escribiendo un nuevo flujo de datos en un archivo.

Puede crear una nueva secuencia en un archivo nuevo o existente mediante la [**función AVIFileCreateStream.**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) Esta función define una nueva secuencia según las características descritas en una estructura [**AVISTREAMINFO,**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) crea una interfaz de secuencia para la nueva secuencia, incrementa el recuento de referencias de la secuencia y devuelve la dirección del puntero de la interfaz de flujo.

Antes de escribir el contenido de la secuencia, debe especificar el formato de secuencia. Puede establecer el formato de secuencia mediante la [**función AVIStreamSetFormat.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) Al establecer el formato de una secuencia de vídeo, debe proporcionar a esta función una estructura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contenga la información adecuada. Al establecer el formato de una secuencia de audio, debe proporcionar una [**estructura WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contenga la información adecuada. La información que necesita proporcionar a la función para otros tipos de secuencia depende del tipo de secuencia y del controlador de secuencias.

Puede escribir el contenido multimedia en una secuencia mediante la [**función AVIStreamWrite.**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) Esta función copia los datos sin procesar de un búfer proporcionado por la aplicación en la secuencia especificada. El controlador de archivos AVI predeterminado anexa información al final de una secuencia. El controlador WAVE predeterminado puede escribir datos de audio de forma de onda dentro de una secuencia, así como al final de una secuencia.

Puede escribir información complementaria sobre el archivo o secuencia que no se incluye en la función [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) o [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) mediante las funciones [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) y [**AVIStreamWriteData.**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) Puede registrar datos aplicables a todo el archivo, como la información de copyright y el historial de modificación, mediante **AVIFileWriteData**. Puede registrar información específica del flujo, como la configuración de compresión y descompresión, mediante **AVIStreamWriteData**. La información complementaria se almacena en fragmentos independientes dentro del archivo.

Puede cerrar la secuencia después de terminar de escribir en la nueva secuencia mediante la [**función AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) Esta función borra los búferes usados para registrar los datos del flujo y completa y cierra los fragmentos de datos incompletos del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones con secuencias](stream-operations.md)
</dt> </dl>

 

 