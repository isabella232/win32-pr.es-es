---
title: Sesiones null
description: A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5476a49513019fe15afa4a30beae08104533a6621a84c4e0d1de4e9f315275ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019565"
---
# <a name="null-sessions"></a>Sesiones null

A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada. En concreto, la llamada a [**la función RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) devuelve el nivel de autenticación y el proveedor de seguridad usados para la llamada. Esta operación no significa que la llamada no se encontraba en una sesión nula. Los dos problemas son ortogonales. En Microsoft Windows 2000, una llamada a procedimiento remoto puede intentar suplantar a un llamador y comprobar los permisos después de la suplantación. En Microsoft Windows XP, es más rápido llamar a la [**función RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) y buscar la **marca NullSession.**

Existe otra diferencia relevante entre Windows 2000 y Windows XP. Si solo se especifica la marca RPC IF ALLOW SECURE ONLY, las llamadas en la sesión null pasan \_ \_ por Windows \_ \_ 2000. En Windows XP, con el ajuste general de la configuración de seguridad predeterminada, cuando se especifica esta marca, las llamadas en la sesión nula se rechazan con acceso denegado. Sin embargo, incluso con la marca RPC IF ALLOW SECURE ONLY, RPC no garantiza el nivel de \_ \_ \_ \_ privilegios del usuario que realiza la llamada. Todas las comprobaciones RPC son que el usuario tiene credenciales válidas. Es posible que el usuario que realiza la llamada use la cuenta de invitado u otras cuentas con pocos privilegios. Asegúrese de que el servidor no asume privilegios elevados una vez que se usa RPC \_ \_ IF ALLOW SECURE \_ \_ ONLY.

 

 




