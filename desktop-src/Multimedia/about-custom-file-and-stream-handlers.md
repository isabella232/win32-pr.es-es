---
title: Acerca de los controladores de archivos y secuencias personalizados
description: Acerca de los controladores de archivos y secuencias personalizados
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Vídeo para Windows (VFW), controladores de archivos personalizados
- Vídeo para Windows (VFW), controladores de flujo personalizados
- Vídeo para Windows (VFW), controladores de archivos
- Vídeo para Windows (VFW), controladores de flujo
- VFW (vídeo para Windows), controladores de archivos personalizados
- VFW (vídeo para Windows), controladores de flujo personalizados
- VFW (vídeo para Windows),controladores de archivos
- VFW (vídeo para Windows),controladores de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719c5312c5ba1e783e0cd4cdb81565f66241e4662772ca441283571f0335fb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145168"
---
# <a name="about-custom-file-and-stream-handlers"></a>Acerca de los controladores de archivos y secuencias personalizados

La aplicación puede usar un controlador de archivos personalizado para leer de un archivo o escribir en un archivo que esté en un formato no estándar. Para ello, la aplicación simplemente usa el nombre del controlador de archivos al abrir el archivo o asignar la interfaz de archivo. A continuación, la biblioteca AVIFile usa las funciones del controlador de archivos en lugar de las de otro controlador de archivos. El formato no estándar aparece como datos AVI estándar para la aplicación o para cualquier otra aplicación mediante el controlador de archivos personalizado.

De forma similar, la aplicación puede usar un controlador de flujo personalizado para leer una secuencia que está en un formato no estándar. Una secuencia , independientemente de si constituye audio, vídeo, MIDI, texto o datos personalizados, es un componente de un archivo AVI. Por ejemplo, un archivo AVI que contiene una secuencia de vídeo, un idioma inglés y un francés consta de tres secuencias. La aplicación puede especificar las secuencias de un archivo AVI para procesar y dirigir cada una de esas secuencias a un controlador que pueda procesar de forma óptima el tipo adecuado de datos multimedia.

> [!Note]  
> Debe colocar controladores de archivos y secuencias personalizados en uno o varios archivos DLL, separados de los archivos de aplicación principales.

 

 

 




