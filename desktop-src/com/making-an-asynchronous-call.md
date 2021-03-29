---
title: Realización de una llamada asincrónica
description: El procedimiento para realizar una llamada sincrónica es sencillo el cliente obtiene un puntero de interfaz en el objeto de servidor y llama a los métodos a través de ese puntero. La llamada asincrónica implica un objeto de llamada, por lo que incluye algunos pasos más.
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22dcd7a6509cd07e12357a96222baa04f9e4c942
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421480"
---
# <a name="making-an-asynchronous-call"></a>Realización de una llamada asincrónica

El procedimiento para realizar una llamada sincrónica es sencillo: el cliente obtiene un puntero de interfaz en el objeto de servidor y llama a los métodos a través de ese puntero. La llamada asincrónica implica un objeto de llamada, por lo que incluye algunos pasos más.

Para cada método en una interfaz sincrónica, la interfaz asincrónica correspondiente implementa dos métodos. Estos métodos adjuntan los prefijos Begin \_ y Finish \_ al nombre del método sincrónico. Por ejemplo, si una interfaz denominada ISimpleStream tiene un método de lectura, la interfaz AsyncISimpleStream tendrá un método de lectura Begin \_ y de finalización \_ . Para comenzar una llamada asincrónica, el cliente llama al método Begin \_ .

**Para comenzar una llamada asincrónica**

1.  Consulte el objeto de servidor para la interfaz [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Si [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve E \_ nointerface, el objeto de servidor no admite la llamada asincrónica.

2.  Llame a [**ICallFactory:: CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) para crear un objeto de llamada correspondiente a la interfaz que desee y, a continuación, libere el puntero a [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).

3.  Si no solicitó un puntero a la interfaz asincrónica desde la llamada a [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), consulte el objeto de llamada de la interfaz asincrónica.

4.  Llame al método Begin adecuado \_ .

El objeto de servidor está procesando la llamada asincrónica y el cliente es libre de realizar otro trabajo hasta que necesita los resultados de la llamada.

Un objeto Call solo puede procesar una llamada asincrónica a la vez. Si el mismo cliente de o un segundo llama a un \_ método Begin antes de que finalice una llamada asincrónica pendiente, el \_ método Begin devolverá una \_ llamada RPC E \_ \_ pendiente.

Si el cliente no necesita los resultados del \_ método Begin, puede liberar el objeto de llamada al final de este procedimiento. COM detecta esta condición y limpia la llamada. \_No se llama al método de finalización y el cliente no obtiene ningún parámetro de salida o valor devuelto.

Cuando el objeto de servidor está listo para devolver el \_ método Begin, indica al objeto de llamada que se ha hecho. Cuando el cliente está listo, comprueba si se ha señalado el objeto de llamada. Si es así, el cliente puede completar la llamada asincrónica.

El mecanismo para esta señalización y comprobación entre el cliente y el servidor es la interfaz [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) en el objeto de llamada. Normalmente, el objeto de llamada implementa esta interfaz mediante la agregación de un objeto de sincronización proporcionado por el sistema. El objeto de sincronización ajusta un identificador de evento, que el servidor señala justo antes de volver del \_ método Begin llamando a [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).

**Para completar una llamada asincrónica**

1.  Consulte el objeto de llamada para la interfaz [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) .

2.  Llame a [**ISynchronize:: wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Si [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) devuelve \_ el tiempo de espera de RPC E \_ , el \_ método Begin no finaliza el procesamiento. El cliente puede continuar con otro trabajo y llamar a **Wait** de nuevo más tarde. No se puede llamar al método de finalización \_ hasta que **Wait** devuelve S \_ OK.

    Si [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) devuelve S \_ OK, el \_ método Begin ha devuelto. Llame al método Finish adecuado \_ .

El \_ método Finish pasa al cliente los parámetros out. El comportamiento de los métodos asincrónicos, incluido el valor devuelto del \_ método Finish, debe coincidir exactamente con el del método sincrónico correspondiente.

El cliente puede liberar el objeto de llamada en cuanto se devuelve el método de finalización \_ , o puede contener un puntero al objeto de llamada para realizar llamadas adicionales. En cualquier caso, el cliente es responsable de liberar el objeto de llamada cuando el objeto ya no se necesita.

Si llama a un método de finalización \_ cuando no hay ninguna llamada en curso, el método devolverá una \_ llamada RPC E \_ \_ completada.

> [!Note]  
> Si los objetos de cliente y de servidor están en el mismo apartamento, no se garantiza que las llamadas a [**ICallFactory:: CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) se realicen correctamente. Si el objeto de servidor no admite la llamada asincrónica en una interfaz determinada, se producirá un error al intentar crear un objeto de llamada y el cliente debe utilizar la interfaz sincrónica.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cancelar una llamada asincrónica](canceling-an-asynchronous-call.md)
</dt> <dt>

[Seguridad del cliente durante una llamada asincrónica](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Suplantación y llamadas asincrónicas](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 