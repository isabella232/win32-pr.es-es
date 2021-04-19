---
description: Aislamiento de errores y Directiva FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Aislamiento de errores y Directiva FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538727"
---
# <a name="fault-isolation-and-failfast-policy"></a>Aislamiento de errores y Directiva FailFast

COM+ realiza comprobaciones de coherencia e integridad interna extensas. Si COM+ encuentra una condición de error interno inesperada, finaliza inmediatamente el proceso. Esta Directiva, denominada *FailFast*, facilita la contención de errores y da como resultado sistemas más confiables y sólidos.

Considere un caso en el que COM+ detecta que una de sus estructuras de datos está en un estado dañado. En este momento, la causa y la magnitud de los daños son desconocidos y, desafortunadamente, COM+ no puede saber hasta qué punto se han distribuido los daños. Sin embargo, aunque COM+ se encuentra en un estado indeterminado, no se ejecuta de forma aislada. Al igual que otros archivos dll, se hospeda en un entorno de proceso y comparte un solo espacio de direcciones con el archivo ejecutable del programa principal y muchos otros archivos dll. Por lo tanto, COM+ supone que se ha dañado todo el proceso y el proceso se termina inmediatamente para impedir que se propague información potencialmente dañada a otros procesos o, peor aún, que permita la confirmación y la permanencia de los datos dañados.

COM+ no permite que las excepciones se propaguen fuera de un contexto. Si se produce una excepción mientras se ejecuta dentro de un contexto de COM+ y la aplicación no detecta la excepción antes de volver del contexto, COM+ detecta la excepción y finaliza el proceso. En este caso, el uso de la Directiva FailFast se basa en la suposición de que la excepción ha puesto el proceso en un estado indeterminado. no es seguro continuar el procesamiento.

Como desarrollador o administrador, debe inspeccionar el registro de la aplicación Visor de eventos para obtener más información sobre cualquier acción de FailFast o errores de aplicación graves.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretar códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



