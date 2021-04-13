---
title: API de servidor DVC
description: Las API de servidor de canal virtual dinámico (DVC) se implementan mediante el servidor de Conexión a Escritorio remoto (RDC) de la conexión.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421286"
---
# <a name="dvc-server-apis"></a>API de servidor DVC

Las API de servidor de canal virtual dinámico (DVC) se implementan mediante el servidor de Conexión a Escritorio remoto (RDC) de la conexión.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

No se admite esta interfaz.

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

No se admite esta interfaz.

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

Esta enumeración no se utiliza.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Cambios de comportamiento en otras API de servidor

-   La API de servidor se ha ampliado con una llamada adicional que abre un canal virtual dinámico (DVC). La llamada adicional se realiza mediante la función [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Al usar esta API con DVC, siempre antepondrá los datos leídos con el [**\_ \_ encabezado de PDU de canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header). Esto significa que cualquier lectura debe realizarse con al menos el bloque de datos de **\_ \_ longitud PDU del canal** pasado como búfer de entrada.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Si el identificador de archivo del DVC se recupera llamando a [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) con el parámetro *WTSVirtualFileHandle*, se aplicará la misma regla. Todas las lecturas incluirán [**el \_ \_ encabezado de PDU de canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)y el búfer de lectura debe tener al menos el tamaño de longitud de la **\_ PDU \_ de canal** .

 

 