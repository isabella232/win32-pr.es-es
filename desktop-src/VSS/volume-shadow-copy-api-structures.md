---
description: Las estructuras siguientes se definen en la API de instantáneas de volumen.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Estructuras de api de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f95527f505430e0283b44d233605febb5695cada3f9740e850945f58e751f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590557"
---
# <a name="volume-shadow-copy-api-structures"></a>Estructuras de api de instantáneas de volumen

Las estructuras siguientes se definen en la API de instantáneas de volumen.



| Estructura                                                           | Descripción                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Contiene información sobre un componente determinado.                                                                                                                                                                                                                       |
| [**PROP DEL \_ ÁREA DE \_ DIFERENCIAS DE VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Describe las asociaciones entre los volúmenes de origen que contienen los datos de archivo originales y los volúmenes que contienen el área de almacenamiento de instantáneas.                                                                                                                                |
| [**VSS \_ DIFF \_ VOLUME \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Describe un volumen de área de almacenamiento de instantáneas.                                                                                                                                                                                                                        |
| [**PROPIEDAD DEL \_ OBJETO MGMT \_ de VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Describe las propiedades de un volumen, un volumen de almacenamiento de instantáneas o un área de almacenamiento de instantáneas.                                                                                                                                                                    |
| [**VSS \_ MGMT \_ OBJECT \_ UNION**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Unión de las estructuras PROP de [**VSS \_ VOLUME \_ PROP,**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop) [**VSS \_ DIFF VOLUME \_ \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)y [**VSS DIFF AREA \_ \_ \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) usadas por la estructura [**\_ VSS MGMT \_ OBJECT \_ PROP.**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) |
| [**PROPIEDAD DE OBJETO DE VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Describe las propiedades de un proveedor, volumen, instantánea o conjunto de instantáneas.                                                                                                                                                                                    |
| [**VSS \_ OBJECT \_ UNION**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Una unión de las [**estructuras PROP de VSS SNAPSHOT \_ \_ y**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) [**VSS PROVIDER \_ \_ PROP,**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) utilizada por la [**estructura PROP de VSS \_ OBJECT. \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                                                                    |
| [**PROVEEDOR DE VSS \_ \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Especifica las propiedades del proveedor de instantáneas.                                                                                                                                                                                                                          |
| [**PROPIEDAD DE INSTANTÁNEA DE VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Contiene las propiedades de un conjunto de instantáneas o instantáneas.                                                                                                                                                                                                        |
| [**PROP DE VOLUMEN DE VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Describe las propiedades de un volumen de origen de instantáneas.                                                                                                                                                                                                            |
| [**INFORMACIÓN DE PROTECCIÓN \_ DE \_ VOLÚMENES DE VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Contiene información sobre el nivel de protección de instantáneas de un volumen.                                                                                                                                                                                                 |



 

 

 



