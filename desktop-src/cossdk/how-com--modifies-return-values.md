---
description: Cómo modifica COM+ los valores devueltos
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Cómo modifica COM+ los valores devueltos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba2b8a9761c7bb669982b47d94b7d522298fa6d557d197d24ea4cb5e56a0df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813826"
---
# <a name="how-com-modifies-return-values"></a>Cómo modifica COM+ los valores devueltos

COM+ nunca cambia el valor devuelto de **un HRESULT** que indica un error, como E \_ UNEXPECTED o E \_ FAIL. Sin embargo, cuando un objeto que usa la funcionalidad COM+ devuelve un valor **HRESULT** que indica que se ha producido correctamente (por ejemplo, S OK, S FALSE o \_ NOERROR), COM+ a veces convierte \_ **el HRESULT** en un código de error COM+ antes de volver al autor de la llamada.

Por ejemplo, cuando una aplicación devuelve S OK después de llamar \_ a [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), si el objeto es la raíz de una transacción que no se puede confirmar, **el HRESULT** se convierte en CONTEXT \_ E \_ ABORTED.

Cuando COM+ convierte un **valor HRESULT,** borra todos los parámetros de salida del método. Se liberan las referencias devueltas y los valores de los punteros de objeto devueltos se establecen en **NULL.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y directiva de conmutación por error](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretación de códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



