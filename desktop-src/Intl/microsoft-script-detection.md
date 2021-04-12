---
description: El servicio de detección de scripts de ELS se denomina detección de scripts de Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Detección de scripts de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155157"
---
# <a name="microsoft-script-detection"></a>Detección de scripts de Microsoft

El servicio de detección de scripts de ELS se denomina detección de scripts de Microsoft. Este servicio permite que las aplicaciones detecten los scripts en los que se escribe el texto. El homólogo National Language support (NLS) de un servicio de detección de scripts es la función [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) . Sin embargo, el servicio ELS también recupera los intervalos de texto que pertenecen a cada sistema de escritura.

## <a name="input-to-microsoft-script-detection"></a>Entrada para la detección de scripts de Microsoft

La entrada del servicio de detección de scripts de Microsoft es texto UTF-16 para el que el servicio determina los intervalos de scripts.

## <a name="output-of-microsoft-script-detection"></a>Salida de la detección de scripts de Microsoft

La salida del servicio de detección de scripts de Microsoft es una matriz de intervalos, cada uno de los cuales contiene una cadena UTF-16 terminada en NULL con el nombre especificado por Unicode del sistema de escritura asociado. El servicio informa de los caracteres comunes normales (Zyyy) y heredados (Qaai) como pertenecientes al intervalo de scripts anterior. Los caracteres comunes y heredados iniciales se indican como pertenecientes al siguiente intervalo de script. Si todos los caracteres del texto de entrada son comunes o se heredan, la salida del servicio es un intervalo único con la cadena vacía como datos.

## <a name="microsoft-script-detection-operation"></a>Operación de detección de scripts de Microsoft

El servicio de detección de scripts de Microsoft asigna los puntos de código que pertenecen al intervalo común al sistema de escritura anterior. Como alternativa, el servicio puede asignar los puntos de código al siguiente sistema de escritura si los puntos de código están al principio de la cadena de entrada. La aplicación no tiene que tratar con el intervalo común.

## <a name="microsoft-script-detection-guid"></a>GUID de detección de scripts de Microsoft

El GUID del servicio Microsoft Detección de idioma se declara en Elssrvc. h, tal como se muestra en el código siguiente.


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los servicios lingüísticos extendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



