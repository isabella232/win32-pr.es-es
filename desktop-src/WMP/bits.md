---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tipo 2 tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- Servicio de transferencia inteligente en segundo plano (BITS)
- BITS (Servicio de transferencia inteligente en segundo plano)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359086"
---
# <a name="bits"></a>BITS

El [servicio de transferencia inteligente en segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) es una característica del sistema operativo Windows. BITS transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información de progreso relacionada con las transferencias. Si desea transferir archivos mediante código de C++, BITS es la tecnología correcta que se va a usar. Si desea transferir archivos mediante código JScript en la Página Web de la tienda en línea, use el administrador de descargas en su lugar.

Dado que el administrador de descargas de Windows Media Player usa BITS, puede realizar los pasos necesarios para configurar los trabajos de copia de BITS de forma que Windows Media Player administre los trabajos. Para ello, debe seguir la Convención descrita en la sección [Convención de trabajo de Windows Media Player bits](windows-media-player-bits-job-convention.md) al agregar los trabajos a la cola de transferencia de bits. En esta sección también se describe un mecanismo para recuperar información sobre los trabajos de BITS de la Página Web de tiendas en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del administrador de descargas**](using-the-download-manager.md)
</dt> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 