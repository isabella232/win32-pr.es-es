---
description: Agregar una letra de unidad a un LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Agregar una letra de unidad a un LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388c59a2e1b719e792855460f45fa0c04add7502f8e06aba56f0416a212a9aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755504"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>Agregar una letra de unidad a un LUN

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Puede asignar letras de unidad a objetos de volumen directamente; sin embargo, si el disco es un objeto LUN, tiene algunos pasos adicionales.

**Para asignar una letra de unidad a un objeto LUN**

1.  Si es necesario, desenmascare el LUN en el host local.
    > [!Note]  
    > No puede realizar operaciones administrativas de software en un objeto LUN sin máscara en otro equipo dentro de la sesión vds actual.

     

2.  [**Invoque el método IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) en el equipo que ejecuta el proveedor de hardware.
3.  Inicialice el LUN como un disco básico como se muestra a continuación:
    1.  [**Invoque el método IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto LUN para consultar la [**interfaz IVdsDisk.**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
    2.  [**Invoque el método IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para crear un paquete básico.
    3.  [**Invoque el método IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para agregar el disco al nuevo paquete.
4.  Cree una partición en el disco y obtenga el objeto de volumen como se muestra a continuación:
    1.  [**Invoque el método IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para crear una partición.
    2.  Invoque el método [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) en el objeto asincrónico devuelto por [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para obtener el identificador de volumen de la [**estructura VDS \_ ASYNC \_ OUTPUT.**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
    3.  Pase el identificador de volumen como parámetro al [**método IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para obtener un puntero de objeto de volumen.
5.  [**Invoque el método IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) para asignar la letra de unidad.

> [!Note]  
> El [**método IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) asigna letras de unidad a las particiones sin volúmenes asociados, como las particiones OEM o ESP. No se puede usar para asignar una letra de unidad a un objeto LUN.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**SALIDA DE \_ VDS ASYNC \_**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
