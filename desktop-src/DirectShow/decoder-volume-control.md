---
description: Control de volumen del descodificador
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Control de volumen del descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423099"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="20c6a-103">Control de volumen del descodificador</span><span class="sxs-lookup"><span data-stu-id="20c6a-103">Decoder Volume Control</span></span>

<span data-ttu-id="20c6a-104">Las aplicaciones controlan el volumen de audio a través de la interfaz [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) .</span><span class="sxs-lookup"><span data-stu-id="20c6a-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="20c6a-105">Se proporciona un controlador de interfaz **IBasicAudio** para KSProxy.</span><span class="sxs-lookup"><span data-stu-id="20c6a-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="20c6a-106">Para que un descodificador controle los comandos de volumen de KSProxy, debe agregar varias claves del registro en su script de configuración y admitir el conjunto de propiedades **\_ Wave de KSPROPSETID** .</span><span class="sxs-lookup"><span data-stu-id="20c6a-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="20c6a-107">Cree algunas nuevas claves del registro para el controlador:</span><span class="sxs-lookup"><span data-stu-id="20c6a-107">Create some new registry keys for the driver:</span></span>


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



<span data-ttu-id="20c6a-108">Para implementar el control de volumen, el controlador también debe admitir **KSPROPSETID \_ Wave**, junto con KsProperty.ID = KsProperty \_ Wave \_ Volume.</span><span class="sxs-lookup"><span data-stu-id="20c6a-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="20c6a-109">Esta propiedad se pasa al controlador a través de los métodos [**IKsPropertySet:: get**](ikspropertyset-get.md) y [**IKsPropertySet:: set**](ikspropertyset-set.md) .</span><span class="sxs-lookup"><span data-stu-id="20c6a-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="20c6a-110">Los campos LeftAttenuation y RightAttentuation especifican los volúmenes de altavoz izquierdo/derecho como valores lineales entre 0x0000 y 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="20c6a-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20c6a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20c6a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c6a-112">Interfaces y especificaciones del descodificador</span><span class="sxs-lookup"><span data-stu-id="20c6a-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



