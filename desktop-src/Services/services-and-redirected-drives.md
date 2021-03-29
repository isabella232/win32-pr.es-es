---
description: Un servicio (o cualquier proceso que se ejecute en un contexto de seguridad diferente) que deba tener acceso a un recurso remoto debe usar el nombre UNC (Convención de nomenclatura universal) para tener acceso al recurso.
ms.assetid: 2582259d-077c-4089-9a87-1a377994f0bd
title: Servicios y unidades redirigidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b1435e69ded3bf13a0869a0b9ad2b90bb4682c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002842"
---
# <a name="services-and-redirected-drives"></a>Servicios y unidades redirigidas

Un servicio (o cualquier proceso que se ejecute en un contexto de seguridad diferente) que deba tener acceso a un recurso remoto debe usar el nombre UNC (Convención de nomenclatura universal) para tener acceso al recurso. El servicio debe tener los privilegios adecuados para tener acceso al recurso. Si un servicio del lado servidor utiliza una conexión RPC, la delegación debe estar habilitada en el servidor remoto.

Las letras de unidad no son globales para el sistema. Cada sesión de inicio de sesión recibe su propio conjunto de Letras de unidad de la a a la Z. Por lo tanto, las unidades redirigidas no se pueden compartir entre procesos que se ejecutan en distintas cuentas de usuario. Además, un servicio (o cualquier proceso que se ejecute en su propia sesión de inicio de sesión) no puede tener acceso a las letras de unidad que se establecieron en una sesión de inicio de sesión diferente.

Un servicio no debe tener acceso directamente a los recursos locales o de red a través de las letras de unidad asignadas, ni debe llamar al comando **net use** para asignar las letras de unidad en tiempo de ejecución. El comando **net use** no se recomienda por varias razones:

-   Las asignaciones de unidad existen entre los contextos de inicio de sesión, por lo que si una aplicación se ejecuta en el contexto de la [cuenta LocalService](localservice-account.md), cualquier otro servicio que se ejecute en ese contexto puede tener acceso a la unidad asignada.
-   Si el servicio proporciona credenciales explícitas a un comando de **uso de red** , esas credenciales podrían compartirse accidentalmente fuera de los límites del servicio. En su lugar, el servicio debe utilizar la [suplantación de cliente](/windows/desktop/SecAuthZ/client-impersonation) para suplantar al usuario.
-   Varios servicios que se ejecutan en el mismo contexto pueden interferir entre sí. Si ambos servicios realizan un **uso neto** explícito y proporcionan las mismas credenciales al mismo tiempo, se producirá un error en un servicio con el error "ya conectado".

Además, un servicio no debe usar las [funciones de red de Windows](/windows/desktop/WNet/windows-networking-functions) para administrar las letras de unidad asignadas. Aunque las funciones de WNet pueden volver correctamente, el comportamiento resultante no es el previsto. Cuando el sistema establece una unidad redirigida, se almacena por usuario. Solo el usuario puede administrar la unidad redirigida. El sistema realiza un seguimiento de las unidades redirigidas según el identificador de seguridad (SID) de inicio de sesión del usuario. El SID de inicio de sesión es un identificador único para la sesión de inicio de sesión del usuario. Un solo usuario puede tener varias sesiones de inicio de sesión simultáneas en el sistema.

Si un servicio está configurado para ejecutarse en una cuenta de usuario, el sistema siempre crea una nueva sesión de inicio de sesión para el usuario e inicia el servicio en esa nueva sesión de inicio de sesión. Por lo tanto, un servicio no puede administrar las asignaciones de unidad establecidas en otras sesiones del usuario.

**Windows Server 2003:** En un equipo que tiene varias interfaces de red (es decir, un equipo de host múltiple), se pueden producir retrasos hasta 60 segundos cuando se usan rutas de acceso UNC para acceder a archivos almacenados en un servidor de bloque de mensajes del servidor (SMB) remoto. Para obtener más información, consulte el [artículo 890553](https://support.microsoft.com/kb/890553) en la Knowledge base de ayuda y soporte técnico.

 

 
