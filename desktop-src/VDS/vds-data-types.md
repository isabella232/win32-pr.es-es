---
description: Los tipos de datos compatibles con VDS definen los valores devueltos de la función, los parámetros de función y los miembros de la estructura. Los tipos de datos definen el tamaño y el significado de estos elementos.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipos de datos de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697686"
---
# <a name="vds-data-types"></a>Tipos de datos de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Los tipos de datos compatibles con VDS definen los valores devueltos de la función, los parámetros de función y los miembros de la estructura. Los tipos de datos definen el tamaño y el significado de estos elementos.



| Tipo de datos                                                                                      | Descripción                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_identificador de objeto VDS \_**<br/> | IDENTIFICADOR de objeto VDS. No se garantiza que estos valores sean únicos en los reinicios. <br/> Este tipo se declara en Vds. h (VdsHwPrv. h para proveedores de hardware) como un GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**identificador de la ruta de acceso de VDS \_ \_**<br/>       | IDENTIFICADOR de la ruta de acceso de VDS para e/s de múltiples rutas (MPIO). <br/> Este tipo se declara en Vds. h (VdsHwPrv. h para proveedores de hardware) como UINT64.<br/>                                      |



 

 

