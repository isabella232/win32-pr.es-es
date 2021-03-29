---
title: Cómo usar la API de cliente de Conexión a Escritorio remoto Broker
description: La API de cliente de Conexión a Escritorio remoto Broker permite a los proveedores de protocolos de terceros aprovechar el agente de conexión para agilizar el control de las conexiones que usan su Protocolo para conectarse a máquinas virtuales o servidores de Escritorio remoto en una granja.
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c931245870cfb72aed54e5aaff24e12d03ddf9e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359324"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a>Cómo usar la API de cliente de Conexión a Escritorio remoto Broker

La API de cliente de Conexión a Escritorio remoto Broker permite a los proveedores de protocolos de terceros aprovechar el agente de conexión para agilizar el control de las conexiones que usan su Protocolo para conectarse a máquinas virtuales o servidores de Escritorio remoto en una granja.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a>Paso 1: obtener la interfaz IConnectionBrokerClient

Una vez inicializado el proveedor de la aplicación o el protocolo, realice los pasos siguientes.

1.  Llame a la función [**CBCreateClientInstance**](cbcreateclientinstance.md) para obtener la interfaz [**IConnectionBrokerClient**](iconnectionbrokerclient.md) .
2.  Mantenga la interfaz [**IConnectionBrokerClient**](iconnectionbrokerclient.md) siempre que la necesite.
3.  Cuando ya no se necesite la interfaz [**IConnectionBrokerClient**](iconnectionbrokerclient.md) , llame al método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .

### <a name="step-2-request-the-target-information"></a>Paso 2: solicitar la información de destino

Cuando el proveedor de protocolo reciba una solicitud de conexión entrante, realice los pasos siguientes para llamar al método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) . Este método obtiene, del agente de conexión, el servidor adecuado al que se redirigirá la conexión.

1.  Cree un evento que se pueda señalizar mediante el [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), o una función similar, para usar para el parámetro *hStatusEvent* .
2.  Asigne memoria para los parámetros *pTargetInfo* y *pResult* . Estos bloques de memoria deben permanecer vigentes hasta que se complete toda la secuencia.
3.  Rellene una estructura de [**\_ \_ información de conexión CB**](cb-connection-info.md) que contenga toda la información sobre la conexión entrante.
4.  Llame al método [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) y pase todos los parámetros necesarios. Este es un método asincrónico que devolverá una instancia de la interfaz [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
5.  Espere a que se establezca el evento *hStatusEvent* .
6.  Siempre que se establezca el evento *hStatusEvent* , llame al método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) para determinar el estado de la solicitud.
7.  Cuando [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) devuelve **la \_ solicitud de estado CB \_ \_ completada**, los parámetros *pTargetInfo* y *pResult* contendrán su información. Puede salir del bucle de espera porque ya no se usará el parámetro *hStatusEvent* .
8.  Utilice la información de la estructura de [**\_ \_ información del destino CB**](cb-target-info.md) representada por el parámetro *pTargetInfo* para determinar a dónde debe redirigirse la conexión entrante.
9.  Libere la interfaz [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
10. Cierre el identificador de evento *hStatusEvent* o puede reutilizarlo para las solicitudes de conexión posteriores.

 

 