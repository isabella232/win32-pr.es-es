---
title: Novedades de la administración de redes
description: Novedades de la administración de redes
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421598"
---
# <a name="whats-new-in-network-management"></a>Novedades de la administración de redes

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 y Windows Server 2012

Microsoft Windows 8 incorpora nuevas características de programación de administración de redes. Estos nuevos elementos amplían la funcionalidad de la administración de redes para crear paquetes de aprovisionamiento para operaciones de unión a un dominio sin conexión al aprovisionar equipos con Windows 8.

A continuación se indican las nuevas funciones de administración de red:

-   [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

A continuación se indican las nuevas estructuras de administración de red:

-   [**PARÁMETROS de aprovisionamiento de NETSETUP \_ \_**](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [**Información de usuario \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

La función [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) se ha mejorado en Windows 8 para admitir un nuevo nivel de información y devolver una estructura de información de [**usuario \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) con información de la cuenta de usuario para una cuenta conectada a una identidad de Internet.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

Microsoft Windows 7 incorpora nuevas características de programación de administración de redes. Estos elementos amplían la funcionalidad de la administración de redes para permitir operaciones de unión al dominio sin conexión al aprovisionar equipos con Windows 7.

A continuación se indican las nuevas funciones de administración de red:

-   [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

Las siguientes funciones de administración de red existentes se han mejorado para admitir opciones adicionales:

-   [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a>Windows Server 2003

Microsoft Windows Server 2003 presenta nuevas características de programación de administración de redes. Estos elementos amplían la funcionalidad de las operaciones de administración de redes en Windows Server 2003 y versiones posteriores.

## <a name="windows-xp"></a>Windows XP

Microsoft Windows XP presenta nuevas características de programación de administración de redes. Estos elementos amplían la capacidad de las operaciones de administración de redes en Windows XP y versiones posteriores.

A continuación se indican las nuevas funciones de administración de red:

-   [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




