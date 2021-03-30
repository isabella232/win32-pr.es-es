---
title: Escribir secuencias en un archivo
description: Escribir secuencias en un archivo
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- AVIFileCreateStream función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790306"
---
# <a name="writing-streams-to-a-file"></a>Escribir secuencias en un archivo

También puede crear un archivo que contenga flujos de datos escribiendo un nuevo flujo de datos en un archivo.

Puede crear una nueva secuencia en un archivo nuevo o existente mediante la función [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) . Esta función define una nueva secuencia de acuerdo con las características descritas en una estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) , crea una interfaz de flujo para la nueva secuencia, incrementa el recuento de referencias de la secuencia y devuelve la dirección del puntero de la interfaz de flujo.

Antes de escribir el contenido de la secuencia, debe especificar el formato de la secuencia. Puede establecer el formato de secuencia mediante la función [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) . Al establecer el formato de un flujo de vídeo, debe proporcionar una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contenga la información adecuada. Al establecer el formato de una secuencia de audio, debe proporcionar una estructura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contenga la información adecuada. La información que necesita proporcionar a la función para otros tipos de flujo depende del tipo de flujo y del controlador de flujo.

Puede escribir el contenido multimedia en una secuencia mediante la función [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) . Esta función copia los datos sin procesar de un búfer proporcionado por la aplicación en la secuencia especificada. El controlador de archivos AVI predeterminado ANEXA información al final de una secuencia. El controlador de onda predeterminado puede escribir datos de audio de forma de onda en una secuencia, así como en el final de una secuencia.

Puede escribir información complementaria sobre el archivo o la secuencia que no está incluida en la función [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) o [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) mediante las funciones [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) y [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) . Puede registrar los datos que se aplican a todo el archivo, como la información de copyright y el historial de modificaciones, mediante **AVIFileWriteData**. Puede registrar información específica de la secuencia, como la configuración de compresión y descompresión, mediante **AVIStreamWriteData**. La información complementaria se almacena en fragmentos independientes dentro del archivo.

Puede cerrar la secuencia después de terminar de escribir en la nueva secuencia mediante la función [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Esta función borra los búferes que se usan para registrar los datos de la secuencia y completa y cierra los fragmentos de datos incompletos del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones con secuencias](stream-operations.md)
</dt> </dl>

 

 