---
title: Cancelación de una llamada asincrónica
description: Un cliente puede cancelar una llamada asincrónica que está en curso si el objeto de llamada implementa la interfaz ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466982"
---
# <a name="canceling-an-asynchronous-call"></a>Cancelación de una llamada asincrónica

Un cliente puede cancelar una llamada asincrónica que está en curso si el objeto de llamada implementa la [**interfaz ICancelMethodCalls.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) Para los objetos que usan la serialización estándar, **ICancelMethodCalls** siempre está disponible para las llamadas serializadas. Para los objetos que usan serialización personalizada o para llamadas a objetos de servidor dentro del mismo apartamento, esta funcionalidad solo está disponible si el objeto de llamada implementa **ICancelMethodCalls**.

El cliente puede cancelar la llamada en cualquier momento, desde que se llama al método Begin \_ hasta que se devuelve el método \_ Finish. Si el cliente cancela la llamada antes de llamar al método Finish, debe llamar al método Finish para limpiar el \_ estado del objeto de \_ llamada. Hasta que el cliente lo haya hecho, las llamadas a cualquier método Begin del objeto de llamada \_ devolverán RPC \_ E CALL \_ \_ PENDING.

**Para cancelar una llamada asincrónica**

1.  Consulte el objeto de llamada para [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).

2.  Llame [**a ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)y, a continuación, llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar el puntero obtenido por la llamada [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el paso 1.

3.  Si el cliente aún no ha llamado al método \_ Finish, llámalo ahora.

No hay ninguna garantía de que el servidor haya detenido realmente la ejecución de la llamada. Si el trabajo adicional del cliente depende de algún estado de servidor que la llamada pueda haber cambiado o no, el cliente debe determinar ese estado antes de continuar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realizar una llamada asincrónica](making-an-asynchronous-call.md)
</dt> </dl>

 

 