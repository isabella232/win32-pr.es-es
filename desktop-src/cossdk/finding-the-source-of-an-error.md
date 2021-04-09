---
description: Buscar el origen de un error
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Buscar el origen de un error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080267"
---
# <a name="finding-the-source-of-an-error"></a>Buscar el origen de un error

Puede diagnosticar el origen y obtener una descripción de los errores de la aplicación mediante COM+ y otras herramientas. Si detecta que el error de aplicación se debe a COM+, puede interpretar el mensaje de error que se ve en el archivo Winerror. h o mediante la utilidad de error Microsoft Visual C++.

Si se produce un error en la aplicación de servidor o se produce un comportamiento inesperado, primero debe determinar dónde se produjo el error. El sistema Visor de eventos realiza un seguimiento de los eventos de aplicación, seguridad y sistema. Muchos errores "silenciosos" se registran aquí. Sin embargo, no todos los errores se muestran en el Visor de eventos.

En primer lugar, debe hacer referencia al registro de la aplicación en el Visor de eventos para comprobar la aplicación asociada con el mensaje de evento. (Dado que también puede archivar registros de eventos, puede realizar el seguimiento de un historial de eventos del error). Al hacer doble clic en una entrada del registro se activa una página de **propiedades de evento** , que proporciona más información sobre el evento del sistema.

Para obtener más información sobre cómo depurar una aplicación COM+, vea [depurar aplicaciones com+](debugging-com--applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y Directiva FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretar códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



