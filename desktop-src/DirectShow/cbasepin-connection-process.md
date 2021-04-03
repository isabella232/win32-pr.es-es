---
description: Proceso de conexión de CBasePin
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Proceso de conexión de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997815"
---
# <a name="cbasepin-connection-process"></a>Proceso de conexión de CBasePin

En esta sección se describe cómo la clase [**CBasePin**](cbasepin.md) implementa el proceso de conexión del PIN.

El administrador de gráficos de filtro inicia todas las conexiones de PIN. Llama al método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) del terminal de salida, especificando el PIN de entrada. El PIN de salida completa la conexión llamando al método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN de entrada. El PIN de entrada puede aceptar o rechazar la conexión.

El administrador de gráficos de filtro también puede especificar un tipo de medio para la conexión. Si es así, los pin intentan conectarse con ese tipo. De lo contrario, los pin deben negociar el tipo. El administrador de gráficos de filtro también puede especificar un tipo de medio *parcial* , que tiene el valor GUID \_ null para el tipo principal, el subtipo o el tipo de formato. En ese caso, los pin intentan coincidir con las partes del tipo de medio que se hayan especificado. el valor null de GUID \_ actúa como carácter comodín.

El método [**CBasePin:: Connect**](cbasepin-connect.md) se inicia comprobando que el pin puede aceptar una conexión. Por ejemplo, comprueba que el PIN no está ya conectado. Delega el resto del proceso de conexión al método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) . **AgreeMediaType** realiza todo lo siguiente.

Si el tipo de medio se especifica por completo, el PIN llama al método [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) para intentar la conexión. De lo contrario, prueba los tipos de medios en el orden siguiente:

1.  Los tipos preferidos del PIN de entrada.
2.  Los tipos preferidos del PIN de salida.

Puede revertir este orden estableciendo la marca [**CBasePin:: m \_ BTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) en **true**.

En cada caso, el PIN llama a [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) para enumerar los tipos de medios. Este método recupera un objeto de enumerador, que se pasa al método [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) . El método **TryMediaTypes** recorre en bucle cada tipo de medio y llama a [**AttemptConnection**](cbasepin-attemptconnection.md) para cada tipo.

Dentro del método [**AttemptConnection**](cbasepin-attemptconnection.md) , el PIN de salida llama a los métodos siguientes:

-   Llama a [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) en sí mismo para comprobar si el PIN de entrada es adecuado.
-   Llama a [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) en sí mismo, para validar el tipo de medio.
-   Llama a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el PIN de entrada. El PIN de entrada usa este método para determinar si debe aceptar la conexión.
-   Llama a [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) en sí mismo para completar la conexión.

Tenga en cuenta lo siguiente:

-   [**CheckConnect**](cbasepin-checkconnect.md) es un método virtual. En la clase base, este método comprueba si las direcciones del PIN son compatibles. Los pin de salida deben conectarse a los pin de entrada y viceversa. La clase de PIN derivada normalmente invalidará este método para realizar otras comprobaciones. Por ejemplo, podría consultar el otro PIN para obtener una interfaz necesaria para la conexión. Si la clase derivada invalida **CheckConnect**, debe llamar también al método [**CBasePin**](cbasepin.md) .
-   [**CheckMediaType**](cbasepin-checkmediatype.md) es un método virtual puro, que la clase derivada debe implementar.
-   [**CompleteConnect**](cbasepin-completeconnect.md) es un método virtual que no hace nada en la clase base. Las clases derivadas pueden invalidar este método para realizar cualquier trabajo adicional necesario para completar la conexión, por ejemplo, para decidir un asignador de memoria.

Si se produce un error en cualquiera de estos pasos, el PIN de salida llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para deshacer los pasos que haya tomado [**CheckConnect**](cbasepin-checkconnect.md).

El método [**ReceiveConnection**](cbasepin-receiveconnection.md) del PIN de entrada llama a los métodos [**CheckConnect**](cbasepin-checkconnect.md), [**CheckMediaType**](cbasepin-checkmediatype.md)y [**CompleteConnect**](cbasepin-completeconnect.md) del PIN de entrada. Si se produce un error en cualquiera de estos, el intento de conexión también produce un error.

En el siguiente diagrama se muestra el proceso de conexión en [**CBasePin**](cbasepin.md):

![proceso de conexión de cbasepin](images/cbasepin-connect.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



