---
title: Cancelar una llamada asincrónica
description: Un cliente puede cancelar una llamada asincrónica que está en curso si el objeto de llamada implementa la interfaz ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149665"
---
# <a name="canceling-an-asynchronous-call"></a>Cancelar una llamada asincrónica

Un cliente puede cancelar una llamada asincrónica que está en curso si el objeto de llamada implementa la interfaz [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . En el caso de los objetos que usan la serialización estándar, **ICancelMethodCalls** siempre está disponible para las llamadas de serialización. En el caso de los objetos que usan el cálculo de referencias personalizado o las llamadas a objetos de servidor dentro del mismo apartamento, esta funcionalidad solo está disponible si el objeto de llamada implementa **ICancelMethodCalls**.

El cliente puede cancelar la llamada en cualquier momento, desde el momento en \_ que se llama al método Begin hasta que el \_ método Finish vuelve. Si el cliente cancela la llamada antes de llamar al \_ método de finalización, debe llamar al \_ método de finalización para limpiar el estado del objeto de llamada. Hasta que el cliente lo haya hecho, todas las llamadas a cualquier \_ método Begin en el objeto Call devolverán una \_ llamada RPC E \_ \_ Pending.

**Para cancelar una llamada asincrónica**

1.  Consulte el objeto de llamada para [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).

2.  Llame a [**ICancelMethodCalls:: CANCEL**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)y llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar el puntero que obtiene la llamada [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el paso 1.

3.  Si el cliente ya no ha llamado al método de finalización \_ , llámelo ahora.

No hay ninguna garantía de que el servidor detuviera realmente la ejecución de la llamada. Si el trabajo del cliente depende de algún estado del servidor que la llamada puede haber cambiado o no, el cliente debe determinar ese estado antes de continuar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realización de una llamada asincrónica](making-an-asynchronous-call.md)
</dt> </dl>

 

 