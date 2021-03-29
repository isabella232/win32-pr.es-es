---
title: Acerca de los controladores de archivos y secuencias personalizados
description: Acerca de los controladores de archivos y secuencias personalizados
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Vídeo para Windows (VFW), controladores de archivos personalizados
- Vídeo para Windows (VFW), controladores de secuencias personalizados
- Vídeo para Windows (VFW), controladores de archivos
- Vídeo para Windows (VFW), controladores de secuencias
- VFW (vídeo para Windows), controladores de archivos personalizados
- VFW (vídeo para Windows), controladores de secuencias personalizados
- VFW (vídeo para Windows), controladores de archivo
- VFW (vídeo para Windows), controladores de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903860"
---
# <a name="about-custom-file-and-stream-handlers"></a>Acerca de los controladores de archivos y secuencias personalizados

La aplicación puede usar un controlador de archivos personalizado para leer de un archivo o escribir en un archivo que se encuentra en un formato no estándar. Para ello, la aplicación simplemente usa el nombre del controlador de archivos al abrir el archivo o asignar la interfaz de archivo. A continuación, la biblioteca AVIFile usa las funciones del controlador de archivos en lugar de las de otro controlador de archivos. El formato no estándar aparece como datos AVI estándar en la aplicación o en cualquier otra aplicación mediante el controlador de archivos personalizado.

Del mismo modo, la aplicación puede usar un controlador de flujo personalizado para leer una secuencia que se encuentra en un formato no estándar. Un flujo, ya sea que constituye audio, vídeo, MIDI, texto o datos personalizados, es un componente de un archivo AVI. Por ejemplo, un archivo AVI que contiene una secuencia de vídeo, una banda sonora en inglés y una banda sonora en francés consta de tres flujos. La aplicación puede especificar las secuencias en un archivo AVI para procesar y dirigir cada una de ellas a un controlador que puede procesar de forma óptima el tipo adecuado de datos multimedia.

> [!Note]  
> Debe colocar los controladores de archivos y secuencias personalizados en uno o varios archivos dll, separados de los archivos de aplicación principales.

 

 

 




