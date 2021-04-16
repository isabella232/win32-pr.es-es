---
description: Las aplicaciones TAPI residen en su propio espacio de proceso.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Información general del proveedor de servicios TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566334"
---
# <a name="tapi-service-provider-overview"></a>Información general del proveedor de servicios TAPI

Las aplicaciones TAPI residen en su propio espacio de proceso. Las aplicaciones TAPI cargan el Tapi32.dll o Tapi3.dll en su proceso y TAPI se comunica con TAPISRV a través de una interfaz RPC privada. Un TSP se ejecuta en el contexto de TAPISRV. Un TSP determinado puede residir en un equipo que no sea el equipo del usuario y al que se tiene acceso mediante un TSP remoto. TAPISRV se implementa como un proceso de servicio en SVCHOST. Un MSP reside en el espacio de proceso de la aplicación y siempre es local.

Se puede considerar que un par de TSP/MSP tiene una ruta de comunicación privada virtual. La información se puede enviar entre los dos búferes opacos que no son interpretados por TAPISRV o por el archivo DLL de TAPI.

Algunos proveedores de servicios implementan operaciones específicas del hardware implicado. TAPI 2. x proporciona acceso a estas operaciones a través de la función [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) o [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . TAPI 3. x expone [interfaces específicas del proveedor](./provider-specific-interfaces.md).

En el diagrama siguiente se ilustra el flujo de controles e información, que muestra un TSP independiente (Unimodem) y un par de TSP/MSP (H. 323).

![inquilino independiente y flujo de control e información de TSP/MSP emparejado](images/tsp-msp1.png)

En el diagrama siguiente se muestra el progreso de una llamada entrante que implica un TSP y un MSP.

![llamada entrante con un TSP y un MSP](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Configuración de llamada entrante

-   El TSP envía un mensaje [**line \_ NEWCALL**](line-newcall.md) a TAPISRV. El [**Estado**](./linecallstate--constants.md) de la llamada es LINECALLSTATE \_ .
-   TAPISRV notifica a los clientes de la llamada.
-   TAPI3 crea el objeto de llamada TAPI y, a continuación, llama a [**ITMSPAddress:: CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), que se implementa mediante el MSP.
-   El MSP crea un objeto de llamada MSP y flujos predeterminados en función de los [**tipos de medios**](./tapimediatype--constants.md) necesarios para la llamada. Devuelve un puntero IUnknown al objeto de llamada MSP.
-   TAPI3 agrega el objeto de llamada MSP en el objeto de llamada TAPI, haciendo que las interfaces como [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) estén disponibles para la aplicación. A continuación, notifica a la aplicación la nueva llamada.

A continuación, la aplicación puede usar métodos como [**ITStream:: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) para completar los preparativos para la finalización de la llamada.

## <a name="incoming-call-completion"></a>Finalización de llamada entrante

-   La aplicación llama a [**ITBasicCallControl:: Answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).
-   TAPI3 llama a [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).
-   TAPISERV llama a [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).
-   El TSP inicia el streaming de llamadas. Normalmente, el TSP envía un mensaje al MSP correspondiente y el MSP inicia las secuencias. En algunas implementaciones de TSP/MSP, el proveedor TSP inicia las secuencias.

## <a name="tspmsp-communication-during-call-progress"></a>Comunicación de TSP/MSP durante el progreso de la llamada

Una vez que la llamada está en curso, el TSP y el MSP se comunican pasando búferes opacos a través de TAPISRV y TAPI3.

-   El TSP envía información al MSP mediante el envío del mensaje [**line \_ SENDMSPDATA**](line-sendmspdata.md) a TAPISRV.
-   El MSP recibe información del TSP a través del método [**ITMSPAddress:: ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) . Si los datos están relacionados con un objeto de llamada MSP, se proporciona un puntero de interfaz al objeto de llamada MSP como parámetro de ese método.
-   El MSP envía información al TSP mediante el envío de un \_ evento de datos de MSP \_ en TAPI 3.
-   El TSP recibe información del MSP a través de la función [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) .

El proceso exacto y el contenido de la comunicación entre los proveedores de servicios es específico de un determinado conjunto de TSP/MSP.

> [!Note]  
> En el caso de las llamadas salientes, el MSP normalmente conoce la llamada antes que el TSP. Si el MSP intenta comunicarse con el TSP antes de que se informe al TSP sobre una llamada, se producirá un error en la comunicación. Cuando el MSP y el TSP necesitan intercambiar información relativa a una llamada específica, el TSP debe iniciar la comunicación.

 

 

 
