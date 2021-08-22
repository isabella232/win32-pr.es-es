---
description: Los tipos de datos admitidos por VDS definen valores devueltos de función, parámetros de función y miembros de estructura. Los tipos de datos definen el tamaño y el significado de estos elementos.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipos de datos VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83a0f3586cb73b823feb6b41990d1f305056a23f9ac0e47ef8fbfc1e4853267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007935"
---
# <a name="vds-data-types"></a>Tipos de datos VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se [reemplaza por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Los tipos de datos admitidos por VDS definen valores devueltos de función, parámetros de función y miembros de estructura. Los tipos de datos definen el tamaño y el significado de estos elementos.



| Tipo de datos                                                                                      | Descripción                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**ID. DE \_ OBJETO VDS \_**<br/> | Id. de objeto VDS. No se garantiza que estos valores sean únicos en los reinicios. <br/> Este tipo se declara en Vds.h (VdsHwPrv.h para proveedores de hardware) como GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**ID. DE RUTA \_ DE ACCESO DE VDS \_**<br/>       | Id. de ruta de acceso VDS para E/S de múltiples rutas (MPIO). <br/> Este tipo se declara en Vds.h (VdsHwPrv.h para proveedores de hardware) como UINT64.<br/>                                      |



 

 

