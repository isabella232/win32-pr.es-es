---
title: Windows táctiles de precisión
description: Windows táctiles de precisión
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb81978c9c9849dfa0d073a4b37af3760d1d4e5bc8e8fa2e81317293db04fc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007905"
---
# <a name="windows-precision-touchpad-devices"></a>Windows táctiles de precisión

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
</dl>

## <a name="description"></a>Descripción

El Windows Precision Touchpad es una nueva clase de dispositivos de entrada que proporcionan una entrada de puntero de alta precisión y funcionalidad de gestos. De forma predeterminada, estos dispositivos generan mensajes de rueda de desplazamiento de precisión ultra alta para el consumo de aplicaciones de escritorio.

## <a name="manifestations"></a>Manifestaciones

Las aplicaciones que no están diseñadas para controlar mensajes de rueda de desplazamiento de precisión ultra alta pueden desplazarse por encima o no desplazarse correctamente.

## <a name="mitigation"></a>Mitigación

Los desarrolladores de aplicaciones deben ver la diferencia de desplazamiento en los mensajes de la rueda de desplazamiento del mouse y modificar sus aplicaciones en consecuencia. sin embargo, mientras tanto, una aplicación puede rechazar los mensajes de rueda de desplazamiento de precisión ultra alta (delta = 1) y optar por recibir mensajes de rueda de desplazamiento de alta precisión (delta = 40) o mensajes de rueda de desplazamiento estándar (delta = 120).

## <a name="solution"></a>Solución

Si la aplicación es capaz de controlar mensajes de rueda de desplazamiento de precisión ultra alta, no es necesario hacer nada, ya que este es el mensaje predeterminado enviado por Windows touchpads de precisión.

Si la aplicación es capaz de controlar mensajes de rueda de desplazamiento de alta precisión, pero no mensajes de rueda de precisión ultra alta, agregue lo siguiente al manifiesto de aplicación:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Si la aplicación no es capaz de controlar mensajes de rueda de desplazamiento de alta precisión o mensajes de rueda de precisión ultra alta, agregue lo siguiente al manifiesto de aplicación para indicar que se desean mensajes de rueda de desplazamiento estándar:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




