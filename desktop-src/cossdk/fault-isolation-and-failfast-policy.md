---
description: Aislamiento de errores y directiva de error
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Aislamiento de errores y directiva de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358900"
---
# <a name="fault-isolation-and-failfast-policy"></a>Aislamiento de errores y directiva de error

COM+ realiza exhaustivas comprobaciones de integridad interna y coherencia. Si COM+ encuentra una condición de error interna inesperada, finaliza inmediatamente el proceso. Esta directiva, denominada *failfast,* facilita la contención de errores y da como resultado sistemas más confiables y sólidos.

Considere un caso en el que COM+ detecta que una de sus estructuras de datos está en un estado dañado. En este momento, se desconoce la causa y la magnitud de los daños y, desafortunadamente, COM+ no puede saber hasta qué punto se ha propagado el daño. Sin embargo, aunque COM+ está en un estado indeterminado, no se ejecuta de forma aislada. Al igual que otros archivos DLL, se hospeda en un entorno de proceso y comparte un único espacio de direcciones con el ejecutable del programa principal y muchos otros archivos DLL. Por lo tanto, COM+ supone que todo el proceso se ha dañado y el proceso se termina inmediatamente para evitar que se propague información potencialmente dañada a otros procesos o, lo que es peor, que permita que los datos dañados se confirman y se hacen duraderos.

COM+ no permite que las excepciones se propaguen fuera de un contexto. Si se produce una excepción mientras se ejecuta dentro de un contexto COM+ y la aplicación no detecta la excepción antes de volver del contexto, COM+ detecta la excepción y finaliza el proceso. El uso de la directiva failfast en este caso se basa en la suposición de que la excepción ha puesto el proceso en un estado indeterminado; no es seguro continuar el procesamiento.

Como desarrollador o administrador, debe inspeccionar el registro de aplicaciones Visor de eventos para obtener más información sobre cualquier acción con error o errores graves de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo com+ modifica los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretación de códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solución de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



