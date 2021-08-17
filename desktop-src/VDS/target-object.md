---
description: Objeto de destino
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objeto de destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b528d66fb789e4d237dacae151c3dda596e834f84f529c3677905672de3b7588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057953"
---
# <a name="target-object"></a>Objeto de destino

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de destino modela un destino iSCSI que se encuentra dentro de un subsistema iSCSI.

Use el [**método IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) para determinar los destinos iSCSI del subsistema. Los llamadores pueden obtener un puntero a un destino específico seleccionando el objeto de destino deseado de la enumeración que devuelve el **método QueryTargets.** Con un objeto de destino, puede establecer el nombre descriptivo del destino y la consulta de las propiedades de destino, los LUN asociados y el subsistema que contiene el destino.

Los equipos host deben iniciar sesión en destinos para acceder a sus LUN asociados. Para realizar un inicio de sesión en un destino, el destino debe tener al menos un portal asociado en uno de sus grupos de portal. La entrada y la salida de los LUN asociados se controlan a través de esta sesión de inicio de sesión.

Las propiedades del objeto de destino incluyen un identificador de objeto, un nombre iSCSI, un nombre descriptivo y una marca habilitada para CHAP.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en proveedores de iSCSI VDS 1.1 y 2.0 | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Enumeraciones asociadas                                                                   | Ninguno.                                                                                                                       |
| Estructuras asociadas                                                                     | [**VDS \_ ISCSI \_ TARGET \_ PROP y**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) [**VDS TARGET \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
