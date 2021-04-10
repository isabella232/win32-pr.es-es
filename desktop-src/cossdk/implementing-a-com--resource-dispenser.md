---
description: Implementación de un dispensador de recursos COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementación de un dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153462"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementación de un dispensador de recursos COM+

En los pasos siguientes se describe un procedimiento general para implementar un dispensador de recursos COM+:

1.  Decida el formato **RESTYPID** que clasifique el modo en que los recursos difieren entre sí.

2.  Use la biblioteca y el archivo de encabezado Mtxdm. h y Mtxdm. lib, respectivamente.

3.  Cree un archivo DLL que implemente la interfaz [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) y la API que desee exponer a las aplicaciones.

4.  En Startup ([*DllMain*](/windows/desktop/Dlls/dllmain) o primera llamada a la API Dispensary), llame a la función [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) . Esto devuelve un puntero a la interfaz [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del administrador del dispensador.

5.  Llame a [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), pasando un puntero a la implementación de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Esto hace que el administrador del dispensador cree un titular (Administrador de agrupación) para el dispensador de recursos y, a continuación, devuelva el puntero a la interfaz [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .

6.  Almacene este puntero para que pueda llamar a [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) y [**IHolder:: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  Ahora puede realizar llamadas a [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) y [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)(en respuesta a las llamadas a la API). **AllocResource** responde inicialmente llamando al método [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , pero las llamadas a **AllocResource** posteriores se prestan desde el creciente grupo de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces dispensadoras de recursos COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
