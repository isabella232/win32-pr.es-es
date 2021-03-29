---
title: Acerca de IWMPPluginEnable
description: Acerca de IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IWMPPluginEnable
- complementos, interfaz IWMPPluginEnable
- Complementos de procesamiento de señal digital, interfaz IWMPPluginEnable
- Complementos DSP, interfaz IWMPPluginEnable
- Interfaz IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993953"
---
# <a name="about-iwmppluginenable"></a>Acerca de IWMPPluginEnable

La interfaz **IWMPPluginEnable** es necesaria para los complementos DSP de Windows Media Player. **IWMPPluginEnable** contiene dos métodos que almacenan si Windows Media Player ha habilitado el complemento DSP. Windows Media Player llama a **IWMPPluginEnable:: SetEnable** cuando crea una instancia del complemento de DSP, pasando un valor de **true** si ha habilitado el complemento o **false** en caso contrario.

Los complementos de DSP pueden permanecer cargados incluso cuando el usuario decide deshabilitarlos. Cuando está deshabilitado, un complemento debe copiar los datos del búfer de entrada en el búfer de salida, realizando solo el procesamiento de la conversión de formato, si procede.

Windows Media Player también llama a este método antes de liberar una instancia del complemento DSP. Esto resulta útil para permitir que los clientes del complemento comprueben si el complemento está habilitado actualmente. Por ejemplo, un complemento de la interfaz de usuario podría cambiar la apariencia de sus controles para avisar al usuario de que el complemento DSP no está conectado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces necesarias**](required-interfaces.md)
</dt> </dl>

 

 




