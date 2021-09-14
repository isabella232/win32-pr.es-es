---
title: Realizar una llamada asincrónica
description: El procedimiento para realizar una llamada sincrónica es sencillo El cliente obtiene un puntero de interfaz en el objeto de servidor y llama a métodos a través de ese puntero. La llamada asincrónica implica un objeto de llamada, por lo que implica algunos pasos más.
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22dcd7a6509cd07e12357a96222baa04f9e4c942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249236"
---
# <a name="making-an-asynchronous-call"></a>Realizar una llamada asincrónica

El procedimiento para realizar una llamada sincrónica es sencillo: el cliente obtiene un puntero de interfaz en el objeto de servidor y llama a métodos a través de ese puntero. La llamada asincrónica implica un objeto de llamada, por lo que implica algunos pasos más.

Para cada método de una interfaz sincrónica, la interfaz asincrónica correspondiente implementa dos métodos. Estos métodos asocian los prefijos Begin \_ y Finish al nombre del método \_ sincrónico. Por ejemplo, si una interfaz denominada ISimpleStream tiene un método Read, la interfaz AsyncISimpleStream tendrá un método Begin Read y \_ Finish \_ Read. Para iniciar una llamada asincrónica, el cliente llama al método \_ Begin.

**Para iniciar una llamada asincrónica**

1.  Consulte el objeto de servidor para la [**interfaz ICallFactory.**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) Si [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve E \_ NOINTERFACE, el objeto de servidor no admite la llamada asincrónica.

2.  Llame [**a ICallFactory::CreateCall para**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) crear un objeto de llamada correspondiente a la interfaz que desee y, a continuación, suelte el puntero a [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).

3.  Si no solicitó un puntero a la interfaz asincrónica desde la llamada a [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), consulte el objeto de llamada para la interfaz asincrónica.

4.  Llame al método Begin \_ adecuado.

El objeto de servidor está procesando ahora la llamada asincrónica y el cliente puede realizar otro trabajo hasta que necesite los resultados de la llamada.

Un objeto de llamada solo puede procesar una llamada asincrónica a la vez. Si el mismo cliente o un segundo llaman a un método Begin antes de que finalice una llamada asincrónica pendiente, el método Begin devolverá \_ \_ RPC E CALL \_ \_ \_ PENDING.

Si el cliente no necesita los resultados del método Begin, puede liberar el objeto \_ de llamada al final de este procedimiento. COM detecta esta condición y limpia la llamada. No se \_ llama al método Finish y el cliente no obtiene ningún parámetro out ni un valor devuelto.

Cuando el objeto de servidor está listo para devolver desde el método Begin, indica al \_ objeto de llamada que está listo. Cuando el cliente está listo, comprueba si se ha señalado el objeto de llamada. Si es así, el cliente puede completar la llamada asincrónica.

El mecanismo para esta señalización y comprobación entre el cliente y el servidor es la [**interfaz ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) en el objeto de llamada. Normalmente, el objeto de llamada implementa esta interfaz agregando un objeto de sincronización proporcionado por el sistema. El objeto de sincronización encapsula un identificador de evento, que el servidor señala justo antes de volver del método Begin mediante una llamada a \_ [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).

**Para completar una llamada asincrónica**

1.  Consulte el objeto de llamada para la [**interfaz ISynchronize.**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize)

2.  Llame [**a ISynchronize::Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Si [**Wait devuelve**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) RPC E \_ \_ TIMEOUT, el método Begin no finaliza el \_ procesamiento. El cliente puede continuar con otro trabajo y volver a llamar a **Wait** más adelante. No puede llamar al método Finish \_ hasta que **Wait** devuelva S \_ OK.

    Si [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) devuelve S \_ OK, se devuelve el método \_ Begin. Llame al método Finish \_ adecuado.

El método Finish \_ pasa al cliente cualquier parámetro out. El comportamiento de los métodos asincrónicos, incluido el valor devuelto del método Finish, debe coincidir exactamente con \_ el del método sincrónico correspondiente.

El cliente puede liberar el objeto de llamada en cuanto se devuelve el método Finish, o puede contener un puntero al objeto de llamada \_ para realizar llamadas adicionales. En cualquier caso, el cliente es responsable de liberar el objeto de llamada cuando el objeto ya no es necesario.

Si llama a un método Finish \_ cuando no hay ninguna llamada en curso, el método devolverá RPC E CALL \_ \_ \_ COMPLETE.

> [!Note]  
> Si los objetos de cliente y servidor están en el mismo apartamento, no se garantiza que las llamadas a [**ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) se realiza correctamente. Si el objeto de servidor no admite llamadas asincrónicas en una interfaz determinada, se producirá un error al intentar crear un objeto de llamada y el cliente debe usar la interfaz sincrónica.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cancelación de una llamada asincrónica](canceling-an-asynchronous-call.md)
</dt> <dt>

[Seguridad de cliente durante una llamada asincrónica](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Suplantación y llamadas asincrónicas](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 