---
title: Conceder el derecho de inicio de sesión como servicio en el equipo host
description: Al instalar un servicio para que se ejecute en una cuenta de usuario de dominio, la cuenta debe tener el derecho de iniciar sesión como servicio en el equipo local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773147"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Conceder el derecho de inicio de sesión como servicio en el equipo host

Al instalar un servicio para que se ejecute en una cuenta de usuario de dominio, la cuenta debe tener el derecho de iniciar sesión como servicio en el equipo local. Tenga en cuenta que este derecho de inicio de sesión solo se aplica al equipo local y debe concederse en la Directiva LSA local de cada equipo host. Este paso no es necesario si el servicio se ejecuta como LocalSystem, que, de forma predeterminada, se concede a este derecho.

Para obtener más información sobre cómo conceder el derecho de inicio de sesión como servicio mediante programación, consulte el [código de ejemplo LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




