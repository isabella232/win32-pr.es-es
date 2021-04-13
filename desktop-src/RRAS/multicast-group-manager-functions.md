---
title: Funciones de administrador de grupo de multidifusión
description: Las siguientes funciones se usan para registrar con el administrador del grupo de multidifusión
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357634"
---
# <a name="multicast-group-manager-functions"></a>Funciones de administrador de grupo de multidifusión

Las siguientes funciones se usan para registrar con el administrador del grupo de multidifusión:

[**MgmRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

Las funciones siguientes se usan para administrar la propiedad de la interfaz:

[**MgmGetProtocolOnInterface**](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

Las funciones siguientes se usan para administrar la pertenencia a grupos:

[**MgmAddGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[**MgmDeleteGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

Las siguientes funciones se usan para obtener entradas de reenvío de multidifusión (MFEs) y estadísticas de MFE:

[**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

La siguiente función se usa para modificar MFEs:

[**MgmSetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

Las siguientes funciones se usan para obtener una lista de los grupos que se han unido:

[**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




