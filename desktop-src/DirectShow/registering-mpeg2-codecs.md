---
description: Registro de códecs MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registro de códecs MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362336"
---
# <a name="registering-mpeg2-codecs"></a>Registro de códecs MPEG2

Este tema solo se aplica Windows XP Media Center Edition.

Windows XP Media Center Edition mantiene dos claves del Registro que usa para determinar qué códec usar para reproducir archivos de audio y vídeo MPEG2. La primera clave del Registro especifica el códec MPEG2 preferido del fabricante del equipo y la segunda enumera todos los códecs compatibles con Media Center que están instalados actualmente en el equipo. Cuando Media Center necesita reproducir un archivo MPEG2, usa el códec preferido del fabricante, si se especifica uno. Si no es así, usa el primer códec compatible con Media Center que aparece en el Registro. Si el registro no especifica códecs preferidos o compatibles, Media Center usa el estándar DirectShow filtro para elegir un códec.

Para asegurarse de que Media Center siempre usa un códec MPEG2 compatible, los fabricantes de equipos de Media Center deben especificar el códec MPEG2 preferido en la siguiente ubicación del Registro:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



Los datos clave deben ser los siguientes:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



El programa de instalación de un códec MPEG2 compatible con Media Center debe registrar el códec mediante la creación de dos instancias de la siguiente clave del Registro: una para el códec de vídeo y otra para el códec de audio:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



Los datos clave deben ser los siguientes:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



