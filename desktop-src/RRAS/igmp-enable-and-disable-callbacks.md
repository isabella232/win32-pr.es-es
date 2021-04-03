---
title: Habilitar y deshabilitar devoluciones de llamada de IGMP
description: El administrador del grupo de multidifusión usa dos devoluciones de llamada a IGMP para coordinar los cambios en la propiedad de la interfaz de IGMP a un protocolo de enrutamiento y de un protocolo de enrutamiento a IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904754"
---
# <a name="igmp-enable-and-disable-callbacks"></a>Habilitar y deshabilitar devoluciones de llamada de IGMP

El administrador del grupo de multidifusión usa dos devoluciones de llamada a IGMP para coordinar los cambios en la propiedad de la interfaz de IGMP a un protocolo de enrutamiento y de un protocolo de enrutamiento a IGMP. Las devoluciones de llamada permiten que IGMP coexista en una interfaz con otro protocolo de enrutamiento, como DVMRP.

Una vez que cambia la propiedad de una interfaz, el administrador del grupo de multidifusión invoca primero la devolución de llamada de [**\_ devolución de \_ \_ llamada IGMP PMGM**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . IGMP debe dejar de agregar y eliminar pertenencias a grupos en la interfaz especificada hasta que el administrador del grupo de multidifusión invoque la devolución de llamada de [**\_ devolución de \_ \_ llamada de IGMP PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .

El administrador del grupo de multidifusión invoca la devolución de llamada de [**PMGM \_ habilitar \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) después de completar el cambio de propiedad de la interfaz.

 

 