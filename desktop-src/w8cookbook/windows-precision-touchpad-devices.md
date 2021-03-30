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
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="2ce67-103">Dispositivos Touchpad de Windows Precision</span><span class="sxs-lookup"><span data-stu-id="2ce67-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="2ce67-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="2ce67-104">Platforms</span></span>

<dl> <span data-ttu-id="2ce67-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2ce67-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="2ce67-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ce67-106">Description</span></span>

<span data-ttu-id="2ce67-107">Touchpad de precisión de Windows es una nueva clase de dispositivos de entrada que proporcionan funcionalidad de movimiento y entrada de puntero de alta precisión.</span><span class="sxs-lookup"><span data-stu-id="2ce67-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="2ce67-108">De forma predeterminada, estos dispositivos generan mensajes de rueda de desplazamiento de precisión ultra alta para el consumo de aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="2ce67-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="2ce67-109">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="2ce67-109">Manifestations</span></span>

<span data-ttu-id="2ce67-110">Las aplicaciones que no están diseñadas para controlar los mensajes de rueda de desplazamiento de precisión ultra alta pueden desplazarse por encima o no desplazarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="2ce67-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="2ce67-111">Mitigación</span><span class="sxs-lookup"><span data-stu-id="2ce67-111">Mitigation</span></span>

<span data-ttu-id="2ce67-112">Los desarrolladores de aplicaciones deben mirar el delta de desplazamiento en los mensajes de la rueda de desplazamiento del mouse y modificar sus aplicaciones en consecuencia. sin embargo, en la versión provisional, una aplicación puede optar por mensajes de rueda de desplazamiento de precisión ultra alta (Delta = 1) y elegir recibir mensajes de rueda de desplazamiento de alta precisión (Delta = 40) o mensajes de rueda de desplazamiento estándar (Delta = 120).</span><span class="sxs-lookup"><span data-stu-id="2ce67-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="2ce67-113">Solución</span><span class="sxs-lookup"><span data-stu-id="2ce67-113">Solution</span></span>

<span data-ttu-id="2ce67-114">Si la aplicación es capaz de controlar los mensajes de la rueda de desplazamiento de precisión muy alta, no es necesario hacer nada, ya que este es el mensaje predeterminado que envían los Touchpad de precisión de Windows.</span><span class="sxs-lookup"><span data-stu-id="2ce67-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="2ce67-115">Si la aplicación es capaz de controlar los mensajes de la rueda de desplazamiento de alta precisión, pero no los mensajes de rueda de precisión muy alta, agregue lo siguiente al manifiesto de aplicación:</span><span class="sxs-lookup"><span data-stu-id="2ce67-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="2ce67-116">Si la aplicación no es capaz de controlar los mensajes de la rueda de desplazamiento de alta precisión o los mensajes con una rueda de precisión muy alta, agregue lo siguiente al manifiesto de aplicación para indicar que se desean mensajes de rueda de desplazamiento estándar:</span><span class="sxs-lookup"><span data-stu-id="2ce67-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




