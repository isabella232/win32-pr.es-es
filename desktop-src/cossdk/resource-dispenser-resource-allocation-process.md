---
description: Proceso de asignación de recursos del distribuidor de recursos
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Proceso de asignación de recursos del distribuidor de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e91802b001bdb8a1af3a933d458c4e9b86b6e3bcd2eb40646e9b64a2e2e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953825"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Proceso de asignación de recursos del distribuidor de recursos

Cada vez que un distribuidor de recursos asigna un recurso de su titular, ocurre lo siguiente:

1.  El dispensador de recursos declara un identificador de tipo de recurso **(RESTYPID),** que describe el tipo de recurso necesario.

2.  El dispensador de recursos llama al método [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) del titular y pasa **este RESTYPID**.

3.  El titular genera una lista de candidatos a partir de los recursos disponibles. Los candidatos son recursos que no están dados de alta en una transacción o que ya están dados de alta en la transacción del objeto que realiza la llamada.

4.  Estos candidatos se pasan individualmente al método [**IDispenserDriver::RateResource,**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) donde se les clasifica (en una escala de 0 a 100) por el modo en que el recurso candidato coincide con el **RESTYPID deseado.**

5.  El titular elige el recurso que el distribuidor de recursos califica como más alto.

6.  El distribuidor de recursos puede finalizar el bucle de clasificación al principio asignando al candidato una clasificación de recursos de 100 (un ajuste perfecto). Normalmente, se reservaría una clasificación de 100 para los recursos candidatos que ya están inscritos correctamente, a menos que el distribuidor de recursos concluya que la alistación es una operación económica. Si todos los recursos candidatos (si existen) tienen la clasificación 0 (inutilizable), se crea un nuevo recurso mediante una llamada a [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).

7.  Si el recurso elegido anteriormente no está ya dado de alta en la transacción del objeto que realiza la llamada, se llama al método [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) del distribuidor de recursos.

8.  La [**llamada al método AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) vuelve al distribuidor de recursos con el recurso inscrito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del distribuidor de recursos com+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Registro de un recurso en una transacción](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Seguimiento de recursos no asignados](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



