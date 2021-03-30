---
title: Dispositivos Touchpad de Windows Precision
description: Dispositivos Touchpad de Windows Precision
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104420126"
---
# <a name="windows-precision-touchpad-devices"></a>Dispositivos Touchpad de Windows Precision

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
</dl>

## <a name="description"></a>Descripción

Touchpad de precisión de Windows es una nueva clase de dispositivos de entrada que proporcionan funcionalidad de movimiento y entrada de puntero de alta precisión. De forma predeterminada, estos dispositivos generan mensajes de rueda de desplazamiento de precisión ultra alta para el consumo de aplicaciones de escritorio.

## <a name="manifestations"></a>Manifestaciones

Las aplicaciones que no están diseñadas para controlar los mensajes de rueda de desplazamiento de precisión ultra alta pueden desplazarse por encima o no desplazarse correctamente.

## <a name="mitigation"></a>Mitigación

Los desarrolladores de aplicaciones deben mirar el delta de desplazamiento en los mensajes de la rueda de desplazamiento del mouse y modificar sus aplicaciones en consecuencia. sin embargo, en la versión provisional, una aplicación puede optar por mensajes de rueda de desplazamiento de precisión ultra alta (Delta = 1) y elegir recibir mensajes de rueda de desplazamiento de alta precisión (Delta = 40) o mensajes de rueda de desplazamiento estándar (Delta = 120).

## <a name="solution"></a>Solución

Si la aplicación es capaz de controlar los mensajes de la rueda de desplazamiento de precisión muy alta, no es necesario hacer nada, ya que este es el mensaje predeterminado que envían los Touchpad de precisión de Windows.

Si la aplicación es capaz de controlar los mensajes de la rueda de desplazamiento de alta precisión, pero no los mensajes de rueda de precisión muy alta, agregue lo siguiente al manifiesto de aplicación:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Si la aplicación no es capaz de controlar los mensajes de la rueda de desplazamiento de alta precisión o los mensajes con una rueda de precisión muy alta, agregue lo siguiente al manifiesto de aplicación para indicar que se desean mensajes de rueda de desplazamiento estándar:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




