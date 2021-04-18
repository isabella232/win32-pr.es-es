---
description: El objeto de proveedor modela el programa responsable de la administración del almacenamiento.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Objeto de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb36517f0091776b9429911212610134f31077a2
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571086"
---
# <a name="provider-object"></a>Objeto de proveedor

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El objeto de proveedor modela el programa responsable de la administración del almacenamiento. Este objeto proporciona acceso a la funcionalidad del proveedor de software y del proveedor de hardware. Los programas de proveedor ejecutan operaciones en dispositivos de software (volúmenes y discos) y dispositivos de hardware (subsistemas de almacenamiento y matrices de unidades detrás de controladores RAID).

VDS registra un objeto de proveedor como un objeto COM en el registro de Windows y usa interfaces contenidas (no agregación) para implementar los objetos restantes, ajustando todas las interfaces y métodos y agregando la funcionalidad de forma condicional. Los objetos e interfaces que están ajustados por el objeto de proveedor difieren en función del tipo de proveedor.

No se puede crear una instancia de un objeto de proveedor directamente desde la aplicación. En su lugar, debe iniciar VDS, obtener un puntero a un objeto de servicio y usar el objeto de servicio para consultar los proveedores conocidos para el host. Para obtener instrucciones sobre la carga de VDS, consulte [objetos de inicio y de servicio](startup-and-service-objects.md).

Use el método [**IVdsService:: QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) para enumerar los programas de proveedor registrados en un host. El primer parámetro del método le permite especificar solo proveedores de software, proveedores de hardware o ambos. Con un objeto de proveedor, puede realizar operaciones en los objetos administrados por ese proveedor. Como se muestra en la siguiente ilustración, puede utilizar los métodos que expone la interfaz [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) para crear y consultar objetos de paquete asociados a proveedores de software. Del mismo modo, puede utilizar los métodos de la interfaz [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) para interactuar con los objetos del subsistema asociados a los proveedores de hardware.

![Diagrama que muestra la bifurcación ' aplicación ' en ' proveedores ', después ' Pack ' o ' subsistema ' y, a continuación, ' ejes '.](images/vdsproviderobject.png)

Las propiedades de objeto incluyen un identificador de objeto GUID persistente que representa un proveedor específico y un segundo GUID que representa la versión del proveedor. Tenga en cuenta que otros identificadores de objeto del modelo de objetos de VDS no son persistentes. Las propiedades restantes de este objeto incluyen un nombre de proveedor, información de versión adicional, el software o hardware de tipo de proveedor), varias marcas y una configuración de la prioridad de recompilación que solo se aplica a los proveedores de software.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas 

| Tipo                                                                                         | Elemento                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Interfaces que siempre solo exponen los proveedores de software                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Interfaces que siempre solo exponen los proveedores de hardware                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Interfaces que puede exponer este objeto                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Interfaces que solo pueden exponer los proveedores de hardware                                    | [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype), [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, windows vista y Windows Server 2003:** no se admite la interfaz [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) .<br/> |
| Interfaces que siempre se implementan pero no se exponen a las aplicaciones                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Interfaces que siempre implementan los proveedores de hardware pero que no se exponen a las aplicaciones | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Interfaces que pueden ser implementadas por proveedores de hardware pero no expuestas a las aplicaciones     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Enumeraciones asociadas                                                                      | [**VDS \_ \_Marca de proveedor**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**\_ \_ \_ marca de proveedor de consultas de VDS**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)y [**\_ \_ tipo de proveedor de VDS**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Estructuras asociadas                                                                        | Ninguno.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> <dt>

[Inicio y objetos de servicio](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

