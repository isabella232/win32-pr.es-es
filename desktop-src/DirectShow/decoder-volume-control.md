---
description: Control de volumen del descodificador
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Control de volumen del descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e96ed9efb17a4fb32c41d8b10313edbe015c202b7f7d1f4287e1af20cca559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953154"
---
# <a name="decoder-volume-control"></a>Control de volumen del descodificador

Las aplicaciones controlan el volumen de audio a través [**de la interfaz IBasicAudio.**](/windows/desktop/api/Control/nn-control-ibasicaudio) Se proporciona un controlador de interfaz **IBasicAudio** para KSProxy. Para que un descodificador controle los comandos de volumen de KSProxy, debe agregar varias claves del Registro en su script de instalación y admitir el conjunto de propiedades **KSPROPSETID \_ Wave.**

Cree algunas claves del Registro nuevas para el controlador:


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



Para implementar el control de volumen, el controlador también debe admitir **KSPROPSETID \_ Wave**, junto con KsProperty.Id = KSPROPERTY \_ WAVE \_ VOLUME. Esta propiedad se pasa al controlador a través de los [**métodos IKsPropertySet::Get**](ikspropertyset-get.md) e [**IKsPropertySet::Set.**](ikspropertyset-set.md) Los campos LeftAttenuation y RightAttentuation especifican los volúmenes de altavoz izquierdo/derecho como valores lineales de 0x0000 a 0xffff.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces y especificaciones del descodificador](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



