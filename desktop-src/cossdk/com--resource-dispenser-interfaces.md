---
description: Interfaces de dispensador de recursos COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Interfaces de dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7fa011681defaddc160e835c7caeb6719054f5e4397903a1716ae76f81c7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991525"
---
# <a name="com-resource-dispenser-interfaces"></a>Interfaces de dispensador de recursos COM+

Los componentes de la aplicación usan los dispensadores de recursos para acceder a la información compartida. Las interfaces descritas en la tabla siguiente proporcionan información de referencia detallada para los desarrolladores de los distribuidores de recursos.



| Interfaces                                                | Descripción                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | El titular del dispensador de recursos llama a esta interfaz para crear, dar de alta, evaluar y destruir un recurso.<br/> |
| [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | Los distribuidores de recursos usan esta interfaz para conectarse al administrador del distribuidor.<br/>                                    |
| [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | Esta interfaz se usa para preparar y controlar los recursos.<br/>                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del distribuidor de recursos com+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Tipos usados en interfaces de dispensador de recursos com+](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




