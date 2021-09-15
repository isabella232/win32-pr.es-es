---
description: Las aplicaciones TAPI residen en su propio espacio de proceso.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Información general sobre el proveedor de servicios TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476308"
---
# <a name="tapi-service-provider-overview"></a>Información general sobre el proveedor de servicios TAPI

Las aplicaciones TAPI residen en su propio espacio de proceso. Las aplicaciones TAPI cargan Tapi32.dll o Tapi3.dll en su proceso, y TAPI se comunica con TAPISRV a través de una interfaz RPC privada. Un TSP se ejecuta en el contexto de TAPISRV. Un TSP determinado puede residir en un equipo que no sea el equipo del usuario y se accede a él mediante un TSP remoto. TAPISRV se implementa como un proceso de servicio dentro de SVCHOST. Un MSP reside dentro del espacio de proceso de la aplicación y siempre es local.

Se puede considerar que un par TSP/MSP tiene una ruta de comunicación privada virtual. La información se puede enviar entre los dos mediante búferes opacos que no son interpretados por TAPISRV o el archivo DLL de TAPI.

Algunos proveedores de servicios implementan operaciones específicas del hardware implicado. TAPI 2.x proporciona acceso a estas operaciones a través de la [**función lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) o [**phoneDevSpecific.**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) TAPI 3.x expone interfaces [específicas del proveedor](./provider-specific-interfaces.md).

En el diagrama siguiente se muestra el flujo de controles e información, que muestra un TSP independiente (Unimodem) y un par TSP/MSP (H.323).

![tsp independiente y flujo de control e información tsp/msp emparejados](images/tsp-msp1.png)

En el diagrama siguiente se muestra el progreso de una llamada entrante que implica un TSP y un MSP.

![llamada entrante con un tsp y un msp](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Instalación de llamadas entrantes

-   El TSP envía un mensaje [**\_ LINE NEWCALL**](line-newcall.md) a TAPISRV. El [**estado de la**](./linecallstate--constants.md) llamada es LINECALLSTATE \_ OFFERING.
-   TAPISRV notifica a los clientes la llamada.
-   TAPI3 crea el objeto TAPI Call y, a continuación, llama a [**ITMSPAddress::CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), que se implementa mediante el MSP.
-   El MSP crea un objeto de llamada MSP y secuencias predeterminadas en función de los tipos [**de medios**](./tapimediatype--constants.md) necesarios para la llamada. Devuelve un puntero IUnknown al objeto de llamada MSP.
-   TAPI3 agrega el objeto de llamada MSP al objeto de llamada TAPI, lo que hace que interfaces como [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) estén disponibles para la aplicación. A continuación, notifica a la aplicación la nueva llamada.

A continuación, la aplicación puede usar métodos [**como ITStream::SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) para completar los preparativos para la finalización de llamadas.

## <a name="incoming-call-completion"></a>Finalización de llamadas entrantes

-   La aplicación llama a [**ITBasicCallControl::Answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).
-   TAPI3 llama [**a lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).
-   TAPISERV llama a [**la línea \_ TSPIAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).
-   El TSP inicia el streaming de llamadas. Normalmente, el TSP envía un mensaje al MSP correspondiente y el MSP inicia las secuencias. En algunas implementaciones de TSP/MSP, el TSP inicia las secuencias.

## <a name="tspmsp-communication-during-call-progress"></a>Comunicación TSP/MSP durante el progreso de la llamada

Una vez que la llamada está en curso, el TSP y el MSP se comunican pasando búferes opacos a través de TAPISRV y TAPI3.

-   El TSP envía información al MSP mediante el envío del mensaje [**\_ LINE SENDMSPDATA**](line-sendmspdata.md) a TAPISRV.
-   El MSP recibe información del TSP a través [**del método ITMSPAddress::ReceiveTSPData.**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) Si los datos están relacionados con un objeto de llamada MSP, se proporciona un puntero de interfaz al objeto de llamada MSP como parámetro de ese método.
-   El MSP envía información al TSP mediante el envío de un evento MSP \_ TSP \_ DATA a TAPI 3.
-   El TSP recibe información del MSP a través de la [**función \_ lineReceiveMSPData de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)

El proceso exacto y el contenido de la comunicación entre proveedores de servicios es específico de un conjunto de TSP/MSP determinado.

> [!Note]  
> En el caso de las llamadas salientes, el MSP normalmente conoce la llamada antes del TSP. Si el MSP intenta comunicarse con el TSP antes de que se informe al TSP sobre una llamada, se producirá un error en la comunicación. Cuando el MSP y el TSP necesitan intercambiar información sobre una llamada específica, el TSP debe iniciar la comunicación.

 

 

 
