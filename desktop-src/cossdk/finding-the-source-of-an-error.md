---
description: Buscar el origen de un error
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Buscar el origen de un error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368f67294491148f9bc85b04ca02ab8e3707eb316261ea50138d7b9c356a2bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954085"
---
# <a name="finding-the-source-of-an-error"></a>Buscar el origen de un error

Puede diagnosticar el origen y obtener una descripción de los errores de la aplicación mediante COM+ y otras herramientas. Si detecta que el error de la aplicación se debe a COM+, puede interpretar el mensaje de error que ve el archivo Winerror.h o mediante la utilidad Microsoft Visual C++ error.

Si se produce un error en la aplicación de servidor o se produce un comportamiento inesperado, primero debe determinar dónde se produjo el error. El sistema Visor de eventos realiza un seguimiento de los eventos de aplicación, seguridad y sistema. Aquí se registran muchos errores "silenciosos". Sin embargo, no todos los errores se muestran en el Visor de eventos.

En primer lugar, debe hacer referencia al registro de la aplicación Visor de eventos para comprobar la aplicación asociada al mensaje de evento. (Dado que también puede archivar registros de eventos, puede realizar un seguimiento de un historial de eventos del error). Al hacer doble clic en una entrada del registro, se activa una página **Propiedades del** evento, que proporciona más información sobre el evento del sistema.

Para obtener más información sobre cómo depurar una aplicación COM+, vea [Depuración de aplicaciones COM+.](debugging-com--applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y directiva de conmutación por error](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretación de códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



