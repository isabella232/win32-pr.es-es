---
description: Referencia de comandos de COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Referencia de comandos de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677191"
---
# <a name="copp-command-reference"></a>Referencia de comandos de COPP

En esta sección se describen los comandos del Protocolo de protección de la salida (COPP). Se definen los siguientes comandos.



| Get-Help              | GUID                             |
|----------------------|----------------------------------|
| Establecer el nivel de protección | **DXVA \_ COPPSetProtectionLevel** |
| Establecer señalización        | **DXVA \_ COPPSetSignaling**       |



 

Establecer nivel de protección (comando)

Establece el nivel de protección para un mecanismo de protección de salida especificado. Dependiendo del conector, es posible que se pueda aplicar más de un mecanismo de protección en el mismo conector, con una configuración diferente para cada mecanismo.

**GUID**: DXVA \_ COPPSetProtectionLevel

**Datos de entrada**: una estructura de [**\_ COPPSetProtectionLevelCmdData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .

Establecer comando de señalización

Especifica información sobre la señal de vídeo que no sea el nivel de protección.

En el caso de CGMS-A, determinados estándares de protección requieren que la señal televsion contenga información sobre la relación de aspecto y otra información dentro de los mismos paquetes de forma de onda de VBI que los bits de CGMS-A. Los televisores pueden mostrarse mal si la información de la relación de aspecto no es coherente con el flujo de vídeo. La aplicación puede usar este comando para especificar la relación de aspecto de modo que el controlador de gráficos pueda generar los paquetes VBI correctos.

Este comando también está diseñado para ser extensible si se requiere información de señal adicional en estándares futuros.

**GUID**: DXVA \_ COPPSetSignaling

**Datos de entrada**: una estructura de [**\_ COPPSetSignalingCmdData de DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



