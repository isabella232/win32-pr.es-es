---
description: Las siguientes estructuras se definen en la API de instantáneas de volumen.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Estructuras de API de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1bb699277faa30c6a570203cd820d552cc9f1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696478"
---
# <a name="volume-shadow-copy-api-structures"></a>Estructuras de API de instantáneas de volumen

Las siguientes estructuras se definen en la API de instantáneas de volumen.



| Estructura                                                           | Descripción                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMPONENTINFO de VSS \_**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Contiene información sobre un componente determinado.                                                                                                                                                                                                                       |
| [**\_prop de \_ área de diferencias de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Describe las asociaciones entre los volúmenes de origen que contienen los datos de archivo originales y los volúmenes que contienen el área de almacenamiento de instantáneas.                                                                                                                                |
| [**\_prop de \_ volumen de diferencia de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Describe un volumen de área de almacenamiento de instantáneas.                                                                                                                                                                                                                        |
| [**\_Prop del \_ objeto de administración de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Describe las propiedades de un volumen, un volumen de almacenamiento de instantáneas o un área de almacenamiento de instantáneas.                                                                                                                                                                    |
| [**\_Unión de \_ objetos de administración de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Una Unión de estructuras de propiedades de [**volumen de VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop), prop de volumen de diferencias de VSS y de propiedades de área de diferencias de VSS utilizadas por la estructura Prop del objeto de administración de [**VSS \_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . [**\_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop) [**\_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) |
| [**\_prop de objeto de VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Describe las propiedades de un proveedor, un volumen, una instantánea o un conjunto de instantáneas.                                                                                                                                                                                    |
| [**\_Unión de objetos de VSS \_**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Unión de las estructuras prop de [**instantánea de VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) y del [**\_ proveedor \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) , utilizadas por la estructura [**\_ \_ Prop del objeto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) .                                                                    |
| [**\_Prop del proveedor de VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Especifica las propiedades del proveedor de instantáneas.                                                                                                                                                                                                                          |
| [**\_prop de instantánea de VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Contiene las propiedades de una instantánea o un conjunto de instantáneas.                                                                                                                                                                                                        |
| [**Prop. de volumen de VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Describe las propiedades de un volumen de origen de instantánea.                                                                                                                                                                                                            |
| [**\_información de \_ protección de volumen de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Contiene información sobre el nivel de protección de instantáneas de un volumen.                                                                                                                                                                                                 |



 

 

 



