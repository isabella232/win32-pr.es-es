---
description: Objeto de controlador
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Objeto de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890417"
---
# <a name="controller-object"></a>Objeto de controlador

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se reemplaza [por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de controlador modela un controlador en un subsistema. Los controladores están contenidos en subsistemas y cada controlador tiene uno o varios puertos de controlador a través de los cuales el equipo host puede escribir y leer desde LUN. Un solo controlador se puede establecer simultáneamente en activo para un LUN e inactivo para otros. Un controlador que está activo para un LUN especificado tiene la responsabilidad de controlar la entrada y salida del LUN. En la ilustración siguiente se muestra esta idea.

![Diagrama que muestra un "Controlador" con un LUN activo a la izquierda y dos LUN activos a la derecha.](images/vdscontroller.png)

**VDS 1.0:** Cada uno de los controladores de un subsistema se establece en activo o inactivo en relación con cada uno de los LUN que el subsistema superficie.

Las aplicaciones VDS usan [**el método IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) para determinar los controladores contenidos en un subsistema específico. Los llamadores pueden obtener un puntero a un controlador específico seleccionando el objeto de controlador deseado de la enumeración devuelta por el **método QueryControllers.** Con un objeto de controlador, un autor de la llamada puede establecer el estado del controlador, consultar sus LUN asociados, consultar sus puertos de controlador y vaciar e invalidar la memoria caché.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto de controlador incluyen el estado y el estado del controlador, y un recuento de los puertos.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                              | Elemento                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                                 | [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| Interfaces que siempre expone este objeto en VDS 1.1 y 2.0 Canal de fibra proveedores de aplicaciones | [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| Interfaces que puede exponer este objeto                                                     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| Enumeraciones asociadas                                                                           | [**VDS \_ ESTADO \_ DEL CONTROLADOR**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).                                                                      |
| Estructuras asociadas                                                                             | [**VDS \_ CONTROLLER \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) [**VDS CONTROLLER \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
