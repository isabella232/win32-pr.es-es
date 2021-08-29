---
description: El servicio de detección de scripts elS se denomina Detección de scripts de Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Detección de scripts de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222578ceab7f476c59293bae8343a2d2809a6b0e90c65eb10957e9e7b9313894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147197"
---
# <a name="microsoft-script-detection"></a>Detección de scripts de Microsoft

El servicio de detección de scripts elS se denomina Detección de scripts de Microsoft. Este servicio permite a las aplicaciones detectar los scripts en los que se escribe texto. El homólogo de National Language Support (NLS) de un servicio de detección de scripts es la [función GetStringScripts.](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) Sin embargo, el servicio ELS recupera además los intervalos de texto que pertenecen a cada sistema de escritura.

## <a name="input-to-microsoft-script-detection"></a>Entrada para la detección de scripts de Microsoft

La entrada al servicio de detección de scripts de Microsoft es texto UTF-16 para el que el servicio determina los intervalos de script.

## <a name="output-of-microsoft-script-detection"></a>Salida de detección de scripts de Microsoft

La salida del servicio Detección de scripts de Microsoft es una matriz de intervalos, cada uno de los que contiene una cadena UTF-16 terminada en NULL con el nombre especificado por Unicode del sistema de escritura asociado. El servicio informa de que los caracteres comunes normales (Zyyy) y heredados (Qaai) pertenecen al intervalo de scripts anterior. Los caracteres comunes y heredados iniciales se notifican como pertenecientes al siguiente intervalo de scripts. Si todos los caracteres del texto de entrada son comunes o se heredan, la salida del servicio es un intervalo único con la cadena vacía como sus datos.

## <a name="microsoft-script-detection-operation"></a>Operación de detección de scripts de Microsoft

El servicio de detección de scripts de Microsoft asigna los puntos de código que pertenecen al intervalo común al sistema de escritura anterior. Como alternativa, el servicio puede asignar los puntos de código al siguiente sistema de escritura si los puntos de código están al principio de la cadena de entrada. La aplicación no tiene que tratar con el intervalo común en absoluto.

## <a name="microsoft-script-detection-guid"></a>GUID de detección de scripts de Microsoft

El GUID del servicio de Detección de idioma Microsoft se declara en Elssrvc.h, como se muestra en el código siguiente.


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los servicios lingüísticos extendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



