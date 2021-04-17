---
description: Controller (objeto)
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Controller (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571424"
---
# <a name="controller-object"></a>Controller (objeto)

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de controlador modela un controlador en un subsistema. Los subsistemas contienen controladores y cada controlador tiene uno o más puertos de controlador a través de los cuales el equipo host puede escribir y leer en los LUN. Un solo controlador se puede establecer simultáneamente en activo para un LUN e inactivo para otros. Un controlador que está activo para un LUN especificado conlleva la responsabilidad de controlar la entrada y la salida del LUN. En la ilustración siguiente se muestra esta idea.

![Diagrama que muestra un ' controlador ' con un LUN activo a la izquierda y dos LUN activos a la derecha.](images/vdscontroller.png)

**VDS 1,0:** Cada uno de los controladores de un subsistema se establece en activo o inactivo con respecto a cada uno de los LUN que el subsistema Surfaces.

Las aplicaciones de VDS usan el método [**IVdsSubSystem:: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) para determinar los controladores que se incluyen en un subsistema específico. Los llamadores pueden obtener un puntero a un controlador específico seleccionando el objeto de controlador deseado de la enumeración devuelta por el método **QueryControllers** . Con un objeto de controlador, un llamador puede establecer el estado del controlador, consultar los LUN asociados, consultar sus puertos de controlador y vaciar e invalidar la memoria caché.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades de objeto de controlador incluyen el estado y el estado del controlador, así como un recuento de los puertos.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                              | Elemento                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                                 | [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| Interfaces que siempre expone este objeto en VDS 1,1 y 2,0 Canal de fibra proveedores | [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| Interfaces que puede exponer este objeto                                                     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| Enumeraciones asociadas                                                                           | [**VDS \_ \_Estado del controlador**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).                                                                      |
| Estructuras asociadas                                                                             | [**VDS \_ Notificación \_ de controlador**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) de VDS y de controlador de [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
