---
title: Sesiones null
description: A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169069"
---
# <a name="null-sessions"></a>Sesiones null

A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada. En concreto, la llamada a [**la función RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) devuelve el nivel de autenticación y el proveedor de seguridad usados para la llamada. Esta operación no significa que la llamada no se encontraba en una sesión nula. Los dos problemas son ortogonales. En Microsoft Windows 2000, una llamada a procedimiento remoto puede intentar suplantar a un llamador y comprobar los permisos después de la suplantación. En Microsoft Windows XP, es más rápido llamar a la [**función RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) y buscar la **marca NullSession.**

Existe otra diferencia relevante entre Windows 2000 y Windows XP. Si solo se especifica la marca RPC IF ALLOW SECURE ONLY, las llamadas en la sesión null pasan por \_ \_ Windows \_ \_ 2000. En Windows XP, con el ajuste general de la configuración de seguridad predeterminada, cuando se especifica esta marca, las llamadas en la sesión nula se rechazan con acceso denegado. Sin embargo, incluso con la marca RPC IF ALLOW SECURE ONLY, RPC no garantiza el nivel de \_ \_ \_ \_ privilegios del usuario que realiza la llamada. Todas las comprobaciones RPC son que el usuario tiene credenciales válidas. Es posible que el usuario que realiza la llamada use la cuenta de invitado u otras cuentas con pocos privilegios. Asegúrese de que el servidor no asume privilegios elevados una vez que se usa RPC \_ \_ IF ALLOW SECURE \_ \_ ONLY.

 

 




