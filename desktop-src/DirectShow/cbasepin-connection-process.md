---
description: Proceso de conexión de CBasePin
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Proceso de conexión de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061372"
---
# <a name="cbasepin-connection-process"></a>Proceso de conexión de CBasePin

En esta sección se describe cómo la [**clase CBasePin**](cbasepin.md) implementa el proceso de conexión de pin.

El Administrador de Graph de filtros inicia todas las conexiones de anclar. Llama al método [**IPin::Conectar**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) del pin de salida, especificando el pin de entrada. El pin de salida completa la conexión llamando al método [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del pin de entrada. El pin de entrada puede aceptar o rechazar la conexión.

El Administrador Graph filtro también puede especificar un tipo de medio para la conexión. Si es así, los pines intentan conectarse con ese tipo. Si no es así, los pines deben negociar el tipo. El Administrador Graph filtro también puede  especificar un tipo de medio parcial, que tiene el valor GUID NULL para el tipo \_ principal, subtipo o tipo de formato. En ese caso, los pines intentan coincidir con las partes del tipo de medio especificadas; el valor GUID \_ NULL actúa como un carácter comodín.

El [**método CBasePin::Conectar**](cbasepin-connect.md) comienza comprobando que el pin puede aceptar una conexión. Por ejemplo, comprueba que el pin no está ya conectado. Delega el resto del proceso de conexión al [**método CBasePin::AgreeMediaType.**](cbasepin-agreemediatype.md) **AgreeMediaType** realiza todo lo siguiente.

Si el tipo de medio está totalmente especificado, el pin llama al método [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) para intentar la conexión. De lo contrario, intenta los tipos de medios en el orden siguiente:

1.  Tipos preferidos de la patilla de entrada.
2.  Tipos preferidos del pin de salida.

Puede invertir este orden estableciendo la marca [**CBasePin::m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) en **TRUE.**

En cada caso, el pin llama [**a IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) para enumerar los tipos de medios. Este método recupera un objeto enumerador, que se pasa al [**método CBasePin::TryMediaTypes.**](cbasepin-trymediatypes.md) El **método TryMediaTypes** recorre en bucle cada tipo de medio y llama a [**AttemptConnection**](cbasepin-attemptconnection.md) para cada tipo.

Dentro del [**método AttemptConnection,**](cbasepin-attemptconnection.md) el pin de salida llama a los métodos siguientes:

-   Llama a [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) en sí mismo para comprobar si el pin de entrada es adecuado.
-   Llama a [**CBasePin::CheckMediaType en**](cbasepin-checkmediatype.md) sí mismo para validar el tipo de medio.
-   Llama a [**IPin::ReceiveConnection en**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) el pin de entrada. El pin de entrada usa este método para determinar si debe aceptar la conexión.
-   Llama a [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) en sí mismo para completar la conexión.

Tenga en cuenta lo siguiente:

-   [**CheckConnect**](cbasepin-checkconnect.md) es un método virtual. En la clase base, este método comprueba si las direcciones del pin son compatibles. Los pines de salida deben conectarse a los pines de entrada y viceversa. La clase de pin derivada normalmente invalidará este método para realizar otras comprobaciones. Por ejemplo, podría consultar el otro pin para una interfaz necesaria para la conexión. Si la clase derivada invalida **CheckConnect**, también debe llamar al [**método CBasePin.**](cbasepin.md)
-   [**CheckMediaType es**](cbasepin-checkmediatype.md) un método virtual puro que la clase derivada debe implementar.
-   [**CompleteConnect**](cbasepin-completeconnect.md) es un método virtual que no hace nada en la clase base. Las clases derivadas pueden invalidar este método para realizar cualquier trabajo adicional necesario para completar la conexión, como decidir un asignador de memoria.

Si se produce un error en cualquiera de estos pasos, el pin de salida llama al método [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) para deshacer los pasos que [**ha realizado CheckConnect.**](cbasepin-checkconnect.md)

El método [**ReceiveConnection**](cbasepin-receiveconnection.md) del pin de entrada llama a los métodos [**CheckConnect,**](cbasepin-checkconnect.md) [**CheckMediaType**](cbasepin-checkmediatype.md)y [**CompleteConnect**](cbasepin-completeconnect.md) del pin de entrada. Si se produce un error en cualquiera de ellos, también se produce un error en el intento de conexión.

En el diagrama siguiente se muestra el proceso de conexión [**en CBasePin**](cbasepin.md):

![Proceso de conexión de cbasepin](images/cbasepin-connect.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



