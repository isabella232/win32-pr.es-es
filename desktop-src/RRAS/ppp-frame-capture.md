---
title: Escritura de un controlador para capturar fotogramas PPP
description: En este documento se explica cómo desarrollar un controlador que pueda capturar fotogramas PPP en Windows Vista antes de comprimirse o cifrarse en la ruta de acceso de envío o después de que se descompriman o descifren en la ruta de acceso de recepción.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769a07811980b20ab076f60cc1e4fd7d9aa227b8eecfa44e71089bc949d0de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789693"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Escritura de un controlador para capturar fotogramas PPP

Cuando Protocolo punto a punto tramas (PPP) se envían a través de un túnel del Protocolo de tunelización de punto a punto (PPTP) con cifrado activado o a través de un túnel del Protocolo de tunelización de nivel 2 (L2TP) que usa IPSec para el cifrado, la utilidad de captura de fotogramas PPP típica solo puede capturar fotogramas PPP que tengan un campo de identidad de protocolo cifrado. En este documento se explica cómo desarrollar un controlador que pueda capturar fotogramas PPP en Windows Vista antes de comprimirse o cifrarse en la ruta de acceso de envío o después de que se descompriman o descifren en la ruta de acceso de recepción.

1.  Escriba un controlador de protocolo NDIS. Para obtener más información, vea Controladores de [protocolo NDIS 6.0](https://msdn.microsoft.com/library/ms795570.aspx) o Controladores de protocolo [NDIS (NDIS 5.1).](https://msdn.microsoft.com/library/ms801145.aspx)
2.  Instale el controlador con una identidad de hardware de "ms \_ netmon". Para obtener instrucciones detalladas sobre cómo instalar el controlador con una identidad de hardware específica, vea la sección [Modelos INF](https://msdn.microsoft.com/library/ms794357.aspx).
    > [!Note]  
    > Cada Windows vista permite la instalación de una sola entidad de controlador que tenga la identidad de hardware "ms \_ netmon". Para instalar otro controlador con esta identidad, se debe desinstalar el primer controlador. Un controlador que se instala sin usar la identidad de hardware "ms netmon" no puede realizar el enlace \_ necesario para capturar fotogramas PPP.

     

3.  El controlador de protocolo debe especificar "ndiswanbh" como interfaz de enlace para capturar fotogramas PPP. Para obtener instrucciones detalladas, vea [Especificar interfaces de enlace.](https://msdn.microsoft.com/library/aa937923.aspx)
4.  La [implementación de ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) en el controlador debe admitir "NdisMediumWan" como parte de la matriz mediana, para que pueda abrir el borde del minipuerto ndiswanbh mediante la función [NdisOpenAdapter.](https://msdn.microsoft.com/library/ms804862.aspx)
5.  Si se llama a la función [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) con el estado NDIS STATUS SUCCESS, el controlador de protocolo debe establecer el OID OID OID CURRENT PACKET FILTER de OID GEN con las marcas \_ \_ [NDIS \_ PACKET TYPE \_ \_ PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) y [NDIS \_ PACKET TYPE ALL \_ \_ \_ LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) en este enlace. [ \_ \_ \_ \_ ](https://msdn.microsoft.com/library/bb314089.aspx) Una vez hecho esto, el controlador de protocolo recibirá los fotogramas PPP descifrados de la capa de tramas PPP en su [función ProtocolReceive.](https://msdn.microsoft.com/library/ms797274.aspx)

> [!Note]  
> Esta información solo se aplica a los controladores de una máquina Windows Vista.

 

 

 




