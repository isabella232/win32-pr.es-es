---
title: Concesión de inicio de sesión como derecho de servicio en el equipo host
description: Al instalar un servicio para que se ejecute en una cuenta de usuario de dominio, la cuenta debe tener el derecho de iniciar sesión como servicio en el equipo local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef53e68feb9312bb8efdca285716aa5b6ea077e2e85f6c5538eb13532b51a8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188959"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Concesión de inicio de sesión como derecho de servicio en el equipo host

Al instalar un servicio para que se ejecute en una cuenta de usuario de dominio, la cuenta debe tener el derecho de iniciar sesión como servicio en el equipo local. Tenga en cuenta que este derecho de inicio de sesión solo se aplica al equipo local y debe concederse en la directiva LSA local de cada equipo host. Este paso no es necesario si el servicio se ejecuta como LocalSystem, al que, de forma predeterminada, se concede este derecho.

Para obtener más información sobre cómo conceder mediante programación el inicio de sesión como un derecho de servicio, vea el código de ejemplo [LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




