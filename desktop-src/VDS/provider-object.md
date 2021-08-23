---
description: El objeto de proveedor modela el programa responsable de la administración del almacenamiento.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Provider (Objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb64d879b8213970edd5887c2d7a217c434ec38a113d2c9f36cd9e1d73e564d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999475"
---
# <a name="provider-object"></a>Provider (Objeto)

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El objeto de proveedor modela el programa responsable de la administración del almacenamiento. Este objeto proporciona acceso a la funcionalidad del proveedor de software y del proveedor de hardware. Los programas de proveedor ejecutan operaciones en dispositivos de software (volúmenes y discos) y dispositivos de hardware (subsistemas de almacenamiento y matrices de unidades detrás de controladores RAID).

VDS registra un objeto de proveedor como un objeto COM en el registro de Windows y usa interfaces contenidas (no agregaciones) para implementar los objetos restantes, encapsulando todas las interfaces y métodos y agregando funcionalidad condicionalmente. Los objetos e interfaces encapsulados por el objeto de proveedor difieren en función del tipo de proveedor.

No se pueden crear instancias de un objeto de proveedor directamente desde la aplicación. En su lugar, debe iniciar VDS, obtener un puntero a un objeto de servicio y usar el objeto de servicio para consultar los proveedores conocidos para el host. Para obtener instrucciones sobre cómo cargar VDS, vea [Objetos de inicio y de servicio.](startup-and-service-objects.md)

Use el [**método IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) para enumerar los programas de proveedor registrados en un host. El primer parámetro del método permite especificar solo proveedores de software, solo proveedores de hardware o ambos. Con un objeto de proveedor, puede realizar operaciones en los objetos administrados por ese proveedor. Como se muestra en la ilustración siguiente, puede usar los métodos expuestos por la interfaz [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) para crear y consultar objetos de paquete asociados a proveedores de software. Del mismo modo, puede usar los métodos de la interfaz [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) para interactuar con los objetos del subsistema asociados a los proveedores de hardware.

![Diagrama que muestra una bifurcación de "Aplicación" en "Providers", luego "Pack" o "Subsystem" y, a continuación, "Ejes".](images/vdsproviderobject.png)

Las propiedades de objeto incluyen un identificador de objeto GUID persistente que representa un proveedor específico y un segundo GUID que representa la versión del proveedor. Tenga en cuenta que otros identificadores de objeto del modelo de objetos VDS no son persistentes. Las propiedades restantes de este objeto incluyen un nombre de proveedor, información de versión adicional, el tipo de proveedor software o hardware), varias marcas y una configuración de prioridad de recompilación que solo se aplica a los proveedores de software.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas. 

| Tipo                                                                                         | Elemento                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Interfaces siempre expuestas por proveedores de software                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Interfaces que siempre exponen los proveedores de hardware únicamente                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Interfaces que puede exponer este objeto                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Interfaces que solo pueden exponer los proveedores de hardware                                    | [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype), [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, Windows Vista y Windows Server 2003:** no se admite la interfaz [**IVdsHwProviderStoragePools.**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)<br/> |
| Interfaces que siempre se implementan pero no se exponen a las aplicaciones                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Interfaces que siempre se implementan mediante proveedores de hardware pero que no se exponen a las aplicaciones | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Interfaces que pueden implementar los proveedores de hardware pero que no se exponen a las aplicaciones     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Enumeraciones asociadas                                                                      | [**VDS \_ PROVIDER \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**VDS QUERY PROVIDER \_ \_ \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)y [**VDS PROVIDER \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Estructuras asociadas                                                                        | Ninguno.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> <dt>

[Objetos de inicio y servicio](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

