---
description: Referencia de comandos copp
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Referencia de comandos copp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1a706863464b6f303e05cb88e28a075dffbfba7b6bf54f8289a2699e66a76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565975"
---
# <a name="copp-command-reference"></a>Referencia de comandos copp

En esta sección se describen los comandos del Protocolo de protección de salida certificado (COPP). Se definen los siguientes comandos.



| Comando              | GUID                             |
|----------------------|----------------------------------|
| Establecer el nivel de protección | **DXVA \_ COPPSetProtectionLevel** |
| Establecer señalización        | **DXVA \_ COPPSetSignaling**       |



 

Comando Establecer nivel de protección

Establece el nivel de protección para un mecanismo de protección de salida especificado. Dependiendo del conector, podría ser posible aplicar más de un mecanismo de protección en el mismo conector, con una configuración diferente para cada mecanismo.

**GUID:** DXVA \_ COPPSetProtectionLevel

**Datos de** entrada: estructura [**\_ COPPSetProtectionLevelCmdData de DXVA.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata)

Establecer comando de señalización

Especifica información sobre la señal de vídeo que no sea el nivel de protección.

Para CGMS-A, ciertos estándares de protección requieren que la señal de televsion contenga información sobre la relación de aspecto y otra información dentro de los mismos paquetes de onda de VBI que los bits de CGMS-A. Las televisión pueden mostrarse mal si la información de relación de aspecto no es coherente con la secuencia de vídeo. La aplicación puede usar este comando para especificar la relación de aspecto para que el controlador de gráficos pueda generar los paquetes de VBI correctos.

Este comando también está diseñado para ser extensible si se requiere información de señal adicional en estándares futuros.

**GUID:** DXVA \_ COPPSetSignaling

**Datos de** entrada: estructura [**\_ DXVA COPPSetSignalingCmdData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



