---
description: Proceso de asignación de recursos del dispensador de recursos
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Proceso de asignación de recursos del dispensador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274946"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Proceso de asignación de recursos del dispensador de recursos

Cada vez que un dispensador de recursos asigna un recurso a su titular, ocurre lo siguiente:

1.  El dispensador de recursos declara un identificador de tipo de recurso (**RESTYPID**), que describe el tipo de recurso necesario.

2.  El dispensador de recursos llama al método [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) del titular, pasando este **RESTYPID**.

3.  El titular genera una lista de candidatos a partir de los recursos disponibles. Los candidatos son recursos que no están inscritos en una transacción o que ya están inscritos en la transacción del objeto que realiza la llamada.

4.  Estos candidatos se pasan individualmente al método [**IDispenserDriver:: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , donde se clasifican (en una escala de 0 a 100) por el grado en que el recurso candidato coincide con el **RESTYPID** deseado.

5.  El titular elige el recurso que el dispensador de recursos es el más alto.

6.  El dispensador de recursos puede finalizar el bucle de clasificación al principio asignando al candidato una clasificación de recursos de 100 (un ajuste perfecto). Normalmente, una clasificación de 100 se reserva para los recursos candidatos que ya están inscritos correctamente, a menos que el dispensador de recursos concluya que la inscripción es una operación económica. Si todos los recursos candidatos (si existen) se clasifican como 0 (inutilizables), se crea un nuevo recurso mediante una llamada a [**IDispenserDriver:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).

7.  Si el recurso elegido anteriormente no está ya dado de alta en la transacción del objeto que realiza la llamada, se llama al método [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) del dispensador de recursos.

8.  La llamada al método [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) devuelve al dispensador de recursos con el recurso dado de alta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Dar de alta un recurso en una transacción](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Seguimiento de recursos no asignados](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



