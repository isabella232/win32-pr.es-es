---
title: API de servidor DVC
description: El servidor de Conexión a Escritorio remoto (RDC) de la conexión implementa las API de servidor de canal virtual dinámico (DVC).
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f43ab4032e4500732e2f9ee6cfa9a2c17f8b1892e55973ba633758792f00bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353978"
---
# <a name="dvc-server-apis"></a>API de servidor DVC

El servidor de Conexión a Escritorio remoto (RDC) de la conexión implementa las API de servidor de canal virtual dinámico (DVC).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

Esta interfaz no se admite.

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

Esta interfaz no se admite.

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

Esta enumeración no se utiliza.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Cambios en el comportamiento de otras API de servidor

-   La API del servidor se ha ampliado con una llamada adicional que abre un canal virtual dinámico (DVC). La llamada adicional se realiza mediante la [**función WTSVirtualChannelOpenEx.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Al usar esta API con DVC, siempre antepone los datos leídos con [**CHANNEL \_ PDU \_ HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header). Esto significa que cualquier lectura debe realizarse con al menos el bloque de datos **CHANNEL \_ PDU \_ LENGTH** pasado como búfer de entrada.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Si se recupera el identificador de archivo para la DVC mediante una llamada a [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) con el parámetro *WTSVirtualFileHandle,* se aplicará la misma regla. Todas las lecturas incluirán [**CHANNEL \_ PDU \_ HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)y el búfer de lectura debe tener al menos el tamaño **CHANNEL \_ PDU \_ LENGTH.**

 

 