---
description: Los nombres del mismo nivel los usan el Protocolo de resolución de nombres del mismo nivel (PNRP), Peer Identity Manager y la infraestructura de agrupación del mismo nivel.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Nombres de mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3587cb27a0d47ebedb60e7987b035a0486e0b67e46fad12fe4673e490268be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775865"
---
# <a name="peer-names"></a>Nombres de mismo nivel

Los nombres del mismo nivel los usan el Protocolo de resolución de nombres del mismo nivel (PNRP), Peer Identity Manager y la infraestructura de agrupación del mismo nivel. Los nombres del mismo nivel son nombres estables para recursos como equipos, usuarios, grupos o servicios. PNRP usa nombres del mismo nivel para identificar los nodos de una red del mismo nivel.

> [!Note]  
> Un punto de conexión que usa la infraestructura del mismo nivel es realmente una tupla que consta de una dirección, puerto y protocolo IPv4 o IPv6 (TCP o UDP). Un nombre del mismo nivel puede tener más de una tupla.

 

Un nombre del mismo nivel es una cadena de texto con el formato siguiente:

-   "Authority.Classifier"

El valor de una autoridad depende de si el nombre es seguro o no seguro. El clasificador de un nombre del mismo nivel es una cadena. Un clasificador puede ser cualquier nombre que contenga 150 caracteres UNICODE o menos. Los nombres del mismo nivel distinguen mayúsculas de minúsculas y se pueden registrar como protegidos o no seguros. En la lista siguiente se identifican algunos ejemplos de nombres del mismo nivel:

-   "0.MyUnsecuredPeerName"
-   "0.JohnDoe.Games"
-   "6520c005f63fc1864b7d8f3cabebd4916ae7f33d. JohnDoe"

## <a name="secure-peer-names"></a>Proteger nombres del mismo nivel

Para un nombre seguro, la autoridad es el hash del algoritmo hash seguro (SHA) de la clave pública del nombre del mismo nivel y da como resultado una cadena hexadecimal de 40 caracteres. El propietario o delegado del propietario del nombre del mismo nivel solo puede registrar un nombre seguro del mismo nivel con PNRP. Se debe crear un nombre protegido del mismo nivel llamando a [**PeerCreatePeerName.**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)

## <a name="unsecured-peer-names"></a>Nombres del mismo nivel no seguros

Para un nombre no seguro, la autoridad es cero (0) y el clasificador es la única parte significativa del nombre del mismo nivel, que crea un nombre de mismo nivel no seguro sin una identidad [asociada.](identity-manager-api.md) Los nombres del mismo nivel no seguros se usan en el registro y la resolución de nombres PNRP. Los nombres del mismo nivel no seguros proporcionan una manera útil de registrar y resolver recursos que no requieren una resolución de nombres segura. Sin embargo, cualquier nodo puede publicar cualquier nombre no seguro. Las aplicaciones que se refieren a la seguridad deben asegurarse de que son sólidas y seguras en su consumo de nombres de mismo nivel no seguros.

> [!Note]  
> Cualquier persona puede registrar un nombre de mismo nivel no seguro con PNRP.

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a>PNRP y la instancia de nombre del mismo nivel más cercana

Puede haber más de una instancia de un nombre del mismo nivel. Cuando se [usa PNRP](pnrp-namespace-provider-api.md) para resolver un nombre  del mismo nivel, hay un concepto de una instancia de nombre del mismo nivel más cercana, lo que significa que el nombre tiene una ubicación de servicio más cercana al miembro **saHint** especificado en [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) o [**PNRPINFO \_ V2.**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)) Si no se proporciona ninguna sugerencia, más cerca de una de las direcciones IP locales.

 

 
