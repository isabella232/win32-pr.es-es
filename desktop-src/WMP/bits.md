---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Reproductor de Windows Media en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- tipo 2 tiendas en línea, Servicio de transferencia inteligente en segundo plano (BITS)
- Servicio de transferencia inteligente en segundo plano (BITS)
- BITS (Servicio de transferencia inteligente en segundo plano)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6f1a9987ca50d659063e9689289334201b0121ccfe5257f71030536eee03a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135978"
---
# <a name="bits"></a>BITS

El [Servicio de transferencia inteligente en segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) es una característica del Windows operativo. BITS transfiere archivos (descargas o cargas) entre un cliente y un servidor, y proporciona información de progreso relacionada con las transferencias. Si desea transferir archivos mediante código de C++, BITS es la tecnología correcta que se va a usar. Si desea transferir archivos mediante el código JScript en la página web de la tienda en línea, use el Administrador de descarga en su lugar.

Dado que Reproductor de Windows Media Download Manager usa BITS, puede tomar medidas para configurar los trabajos de copia de BITS de forma que Reproductor de Windows Media los trabajos. Para ello, debe seguir la convención descrita en la sección Reproductor de Windows Media trabajo [de BITS](windows-media-player-bits-job-convention.md) al agregar los trabajos a la cola de transferencia de BITS. En esta sección también se describe un mecanismo para recuperar información sobre los trabajos de BITS desde la página web de las tiendas en línea.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del Administrador de descargas**](using-the-download-manager.md)
</dt> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 