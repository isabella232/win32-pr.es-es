---
title: Acerca de IWMPPluginEnable
description: Acerca de IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Reproductor de Windows Media complementos, interfaces
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- Complementos de DSP, interfaces
- interfaces, complementos DSP
- Reproductor de Windows Media complementos, interfaz IWMPPluginEnable
- complementos, interfaz IWMPPluginEnable
- complementos de procesamiento de señal digital, interfaz IWMPPluginEnable
- Complementos DE DSP, interfaz IWMPPluginEnable
- Interfaz IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa64c811bbc981114f47b6fee15af29a6402594eabec2b857d0098adb8db747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470485"
---
# <a name="about-iwmppluginenable"></a>Acerca de IWMPPluginEnable

La **interfaz IWMPPluginEnable** es necesaria para Reproductor de Windows Media de DSP. **IWMPPluginEnable** contiene dos métodos que almacenan si Reproductor de Windows Media ha habilitado el complemento DSP. Reproductor de Windows Media llama a **IWMPPluginEnable::SetEnable** cuando crea una instancia del complemento DSP, pasando un valor de **TRUE** si ha habilitado el complemento o **FALSE** de lo contrario.

Los complementos de DSP pueden permanecer cargados incluso cuando el usuario decide deshabilitarlos. Cuando se deshabilita, un complemento debe copiar datos del búfer de entrada al búfer de salida, realizando solo el procesamiento de conversión de formato, si procede.

Reproductor de Windows Media llama a este método antes de liberar una instancia del complemento DSP. Esto es útil para permitir que los clientes del complemento comprueben si el complemento está habilitado actualmente. Por ejemplo, un complemento de interfaz de usuario podría cambiar la apariencia de sus controles para avisar al usuario de que el complemento DSP no está conectado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces necesarias**](required-interfaces.md)
</dt> </dl>

 

 




