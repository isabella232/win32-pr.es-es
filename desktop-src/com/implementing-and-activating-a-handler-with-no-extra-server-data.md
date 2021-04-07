---
title: Implementar y activar un controlador sin datos de servidor adicionales
description: Implementar y activar un controlador sin datos de servidor adicionales
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6866b40e1257a865aa5068ffd46611c411498877
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104003257"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>Implementar y activar un controlador sin datos de servidor adicionales

Para crear una instancia del controlador, si es una que no obtiene datos de servidor adicionales, el servidor debe implementar [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) pero no [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). **IStdMarshalInfo** tiene un método, [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), que recupera el CLSID del controlador de objetos que se va a usar en el proceso de destino. COM lo llama cuando llama a [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) para usted y activa el controlador en el lado cliente.

A continuación, las implementaciones del servidor y del controlador deben llamar a la función [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) . Esta función crea un serializador estándar en cada lado (denominado administrador de proxy en el lado cliente y un administrador de código auxiliar en el lado servidor).

El servidor llama a [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), pasando el marcador SMEXF \_ Server. Esto crea un contador de referencias estándar del lado servidor (Administrador de código auxiliar). La estructura del lado servidor se muestra en la siguiente ilustración:

![Diagrama que muestra la estructura del lado servidor.](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Estructura de Server-Side

El controlador llama a [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), pasando el controlador de marcador SMEXF \_ . Esto crea un serializador estándar del lado cliente (Administrador de proxy) y lo agrega con el controlador en el lado cliente. La duración de ambos se administra mediante el objeto de identidad de control (que implementa [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) que el sistema implementa cuando el controlador llama a **CoGetStdMarshalEx**. La estructura del lado cliente se muestra en la siguiente ilustración.

![Diagrama que muestra la estructura del lado cliente.](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Estructura de Client-Side

Tal y como se muestra en la ilustración anterior, el controlador se presenta en forma de sándwich entre el administrador del proxy y la identidad o el control desconocido. Esto proporciona al control del sistema la duración del objeto, a la vez que proporciona al controlador el control sobre las interfaces expuestas. La línea discontinua entre el administrador de identidades y el proxy indica que los dos comparten una estrecha integración a través de interfaces privadas internas.

Cuando COM llama a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) para el cliente, crea la instancia de controlador y la agrega con la identidad. El controlador creará el serializador estándar (a través de la llamada a [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), pasando el control desconocido recibido cuando se creó). El controlador no implementa [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , sino que solo devuelve **IMarshal** del serializador estándar. Incluso si el controlador implementa **IMarshal**, no se le llamará durante una conversión de referencias.

Si dos subprocesos anulan simultáneamente la serialización del mismo objeto por primera vez, es posible que se creen temporalmente dos controladores. Posteriormente, se liberará uno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 