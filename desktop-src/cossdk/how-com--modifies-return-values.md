---
description: Cómo modifica COM+ los valores devueltos
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Cómo modifica COM+ los valores devueltos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153204"
---
# <a name="how-com-modifies-return-values"></a>Cómo modifica COM+ los valores devueltos

COM+ nunca cambia el valor devuelto de un **HRESULT** que indica un error, como e \_ inesperado o \_ error. Sin embargo, cuando un objeto que usa la funcionalidad de COM+ devuelve un valor **HRESULT** que indica que se ha realizado correctamente (por ejemplo \_ , S OK, s \_ false o NoError), com+ convierte a veces el **HRESULT** en un código de error de com+ antes de que vuelva al autor de la llamada.

Por ejemplo, cuando una aplicación devuelve S \_ OK después de llamar a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), si el objeto es la raíz de una transacción que no se puede confirmar, el **valor HRESULT** se convierte en el contexto \_ E \_ anulado.

Cuando COM+ convierte un valor **HRESULT** , borra todos los parámetros de salida del método. Se liberan las referencias devueltas y los valores de los punteros de objeto devueltos se establecen en **null**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y Directiva FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretar códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



