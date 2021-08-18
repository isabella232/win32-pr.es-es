---
description: Implementación de un dispensador de recursos COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementación de un dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9c37de2a4910af908bdc3f2e38f1c1b55699b133a59a818b8a09236f8c0a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547897"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementación de un dispensador de recursos COM+

En los pasos siguientes se describe un procedimiento general para implementar un dispensador de recursos COM+:

1.  Decida el **formato RESTYPID** que clasifica cómo se diferencian entre sí los recursos.

2.  Use el archivo de encabezado Mtxdm.h y Mtxdm.lib y la biblioteca, respectivamente.

3.  Compile un archivo DLL que implemente la [**interfaz IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) y la API que desea exponer a las aplicaciones.

4.  En el inicio [*(DllMain o*](/windows/desktop/Dlls/dllmain) la primera llamada a la API de dispensador), llame a la [**función GetDispenserManager.**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) Esto devuelve un puntero a la interfaz [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del administrador del dispensador.

5.  Llame [**a IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser)y pase un puntero a la implementación de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Esto hace que el administrador de dispensador cree un titular (administrador de agrupación) para el dispensador de recursos y, a continuación, devuelva el puntero a la [**interfaz IHolder.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)

6.  Almacene este puntero para que pueda llamar a [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  Ahora puede (en respuesta a las llamadas a la API) realizar llamadas a [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) y [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). **AllocResource responde** inicialmente llamando de nuevo al método [**CreateResource,**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) pero las llamadas **a AllocResource** posteriores se atendidas desde el creciente grupo de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos com+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces de dispensador de recursos COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
