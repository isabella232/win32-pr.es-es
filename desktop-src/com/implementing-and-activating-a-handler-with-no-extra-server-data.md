---
title: Implementar y activar un controlador sin datos de servidor adicionales
description: Implementar y activar un controlador sin datos de servidor adicionales
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81df2bcaf1b50a0727127c4008d9763b76e05e4f2a5d80bf4b282bbbe02e5bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070874"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>Implementar y activar un controlador sin datos de servidor adicionales

Para crear una instancia del controlador, si es una que no obtiene datos de servidor adicionales, el servidor debe implementar [**IStdMarshalInfo,**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) pero no [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). **IStdMarshalInfo tiene** un método, [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), que recupera el CLSID del controlador de objetos que se usará en el proceso de destino. COM llama a esto cuando llama automáticamente [**a CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) y activa el controlador en el lado cliente.

A continuación, las implementaciones del servidor y del controlador deben llamar a la [**función CoGetStdMarshalEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) Esta función crea un serializador estándar en cada lado (denominado administrador de proxy en el lado cliente y un administrador de código auxiliar en el lado servidor).

El servidor llama [**a CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)y pasa la marca SFANF \_ SERVER. Esto crea un serializador estándar del lado servidor (administrador de código auxiliar). La estructura del lado servidor se muestra en la ilustración siguiente:

![Diagrama que muestra la estructura del lado servidor.](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Server-Side estructura

El controlador llama [**a CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)y pasa la marca SLDAF \_ HANDLER. Esto crea un serializador estándar del lado cliente (administrador de proxy) y lo agrega con el controlador en el lado cliente. La duración de ambos se administra mediante el objeto de identidad de control (implementando [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) que el sistema implementa cuando el controlador llama a **CoGetStdMarshalEx**. La estructura del lado cliente se muestra en la ilustración siguiente.

![DIagram que muestra la estructura del lado cliente.](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Client-Side estructura

Como se muestra en la ilustración anterior, el controlador se intercala realmente entre el administrador de proxy y la identidad o el control desconocido. Esto proporciona al sistema control sobre la duración del objeto al tiempo que proporciona al controlador control sobre las interfaces expuestas. La línea discontinua entre identity y proxy Manager indica que ambos comparten una estrecha integración a través de interfaces privadas internas.

Cuando COM llama [**a CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) para el cliente, crea la instancia del controlador y la agrega a identity. El controlador creará el serializador estándar (a través de la llamada a [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), pasando el control desconocido que recibió cuando se creó). El controlador no implementa [**IMarshal,**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) sino que simplemente devuelve **IMarshal desde** el serializador estándar. Incluso si el controlador implementa **IMarshal**, no se llamará durante un unmarshal.

Si dos subprocesos deshabilitan simultáneamente el mismo objeto por primera vez, es posible que dos controladores se cree temporalmente. Posteriormente se lanzará uno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 