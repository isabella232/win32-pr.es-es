---
description: Objeto de destino
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objeto de destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697687"
---
# <a name="target-object"></a>Objeto de destino

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de destino modela un destino iSCSI que está incluido en un subsistema iSCSI.

Use el método [**IVdsSubSystemIscsi:: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) para determinar los destinos iSCSI del subsistema. Los llamadores pueden obtener un puntero a un destino específico seleccionando el objeto de destino deseado de la enumeración devuelta por el método **QueryTargets** . Con un objeto de destino, puede establecer el nombre descriptivo y la consulta del destino para las propiedades de destino, los LUN asociados y el subsistema que contiene el destino.

Los equipos host deben iniciar sesión en los destinos para tener acceso a los LUN asociados. Para realizar un inicio de sesión en un destino, el destino debe tener al menos un portal asociado en uno de sus grupos de portal. La entrada y la salida de los LUN asociados se administran a través de esta sesión de inicio de sesión.

Las propiedades del objeto de destino incluyen un identificador de objeto, un nombre iSCSI, un nombre descriptivo y una marca habilitada para CHAP.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0 | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Enumeraciones asociadas                                                                   | Ninguno.                                                                                                                       |
| Estructuras asociadas                                                                     | [**VDS \_ \_ \_ Propuesta de destino iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) y [**\_ \_ notificación de destino de VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
