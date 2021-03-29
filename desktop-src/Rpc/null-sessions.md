---
title: Sesiones nulas
description: A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486991"
---
# <a name="null-sessions"></a>Sesiones nulas

A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada. Concretamente, al llamar a la función [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) se devuelve el nivel de autenticación y el proveedor de seguridad utilizados para la llamada. Esta operación no significa que la llamada no estuviera en una sesión nula. Los dos problemas son ortogonales. En Microsoft Windows 2000, una llamada a procedimiento remoto puede intentar suplantar a un llamador y comprobar los permisos después de la suplantación. En Microsoft Windows XP, es más rápido llamar a la función [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) y comprobar la marca **NullSession** .

Existe otra diferencia importante entre Windows 2000 y Windows XP. Si solo \_ \_ se especifica la marca RPC si se permite la opción permitir \_ \_ solo protección, las llamadas en la sesión nula pasan en Windows 2000. En Windows XP, con el ajuste general de la configuración de seguridad predeterminada, cuando se especifica esta marca, se rechazan las llamadas en la sesión nula con acceso denegado. Sin embargo, incluso con el \_ uso de la marca RPC si \_ permitir \_ \_ solo protección, RPC no garantiza el nivel de privilegios del usuario que realiza la llamada. Todas las comprobaciones de RPC son que el usuario tiene credenciales válidas. Es posible que el usuario que realiza la llamada esté usando la cuenta invitado u otras cuentas con pocos privilegios. Asegúrese de que el servidor no asuma un privilegio alto una vez que \_ \_ se use RPC si permitir \_ \_ solo protección.

 

 




