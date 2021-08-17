---
description: Agregar discos externos a un paquete
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Agregar discos externos a un paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b83dd76cdc3f1637c07d8d9d818fdaf61fb093151f23aea06f0e9c7f81d6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755460"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Agregar discos externos a un paquete

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Normalmente, un disco externo es un disco dinámico que se asigna en un equipo y se mueve físicamente a otro equipo. Sin embargo, cualquier disco que pertenezca a un paquete que no sea el paquete en línea se considera un disco externo que pertenece a un paquete de disco externo.

Un paquete externo tiene la **marca \_ VDS PKF \_ FOREIGN** establecida en el **miembro ulFlags** de la [**estructura VDS PACK \_ \_ PROP.**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) Los paquetes externos siempre están sin conexión.

En el procedimiento siguiente se describe cómo importar uno o varios discos externos.

**Para importar uno o varios discos externos**

1.  Mueva los discos al nuevo equipo.
2.  En el nuevo equipo, use el [**método IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) para instalar los discos externos.
3.  Seleccione el paquete en línea para que sea el paquete de destino que recibe los discos externos. Si no existe ningún paquete en línea, use el [**método IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para crear un nuevo paquete vacío.
4.  Use el [**método IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) para importar los discos al nuevo paquete dinámico.
5.  Use el [**método IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) para enumerar los paquetes e [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) para determinar qué paquete es ahora el paquete en línea.

Si crea un nuevo paquete de destino vacío, los discos externos no se migran realmente a ese paquete. En su lugar, el paquete externo se marca en línea, la marca **\_ VDS PKF \_ FOREIGN** del paquete se borra (por lo que el paquete ya no es externo) y se descarta el paquete de destino que ha creado.

> [!Note]  
> Use el [**método IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para agregar discos sin asignar (discos no reclamados por un proveedor) a un paquete. Un disco sin asignar no puede ser externo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
