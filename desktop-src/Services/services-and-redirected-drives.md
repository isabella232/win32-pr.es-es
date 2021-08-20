---
description: Un servicio (o cualquier proceso que se ejecute en un contexto de seguridad diferente) que deba tener acceso a un recurso remoto debe usar el nombre de convención de nomenclatura universal (UNC) para acceder al recurso.
ms.assetid: 2582259d-077c-4089-9a87-1a377994f0bd
title: Servicios y unidades redirigidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09073dd4ce1e98c72d027038638428d9b9ff67ae3697663661404464419341a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967112"
---
# <a name="services-and-redirected-drives"></a>Servicios y unidades redirigidas

Un servicio (o cualquier proceso que se ejecute en un contexto de seguridad diferente) que deba tener acceso a un recurso remoto debe usar el nombre de convención de nomenclatura universal (UNC) para acceder al recurso. El servicio debe tener los privilegios adecuados para acceder al recurso. Si un servicio del lado servidor usa una conexión RPC, la delegación debe estar habilitada en el servidor remoto.

Las letras de unidad no son globales para el sistema. Cada sesión de inicio de sesión recibe su propio conjunto de letras de unidad de A a Z. Por lo tanto, las unidades redirigidas no se pueden compartir entre procesos que se ejecutan en diferentes cuentas de usuario. Además, un servicio (o cualquier proceso que se ejecute dentro de su propia sesión de inicio de sesión) no puede tener acceso a las letras de unidad que se establecieron dentro de una sesión de inicio de sesión diferente.

Un servicio no debe acceder directamente a los recursos locales o de red a través de letras de unidad asignadas, ni debe llamar al comando **net use** para asignar letras de unidad en tiempo de ejecución. El **comando net use** no se recomienda por varias razones:

-   Existen asignaciones de unidades en contextos de inicio de sesión, por lo que si una aplicación se ejecuta en el contexto de la cuenta [LocalService](localservice-account.md), cualquier otro servicio que se ejecute en ese contexto puede tener acceso a la unidad asignada.
-   Si el servicio proporciona credenciales explícitas a un comando **net use,** esas credenciales podrían compartirse accidentalmente fuera de los límites del servicio. En su lugar, el servicio debe usar [la suplantación de cliente](/windows/desktop/SecAuthZ/client-impersonation) para suplantar al usuario.
-   Varios servicios que se ejecutan en el mismo contexto pueden interferir entre sí. Si ambos servicios realizan un uso **net** explícito y proporcionan las mismas credenciales al mismo tiempo, un servicio producirá un error "ya conectado".

Además, un servicio no debe usar las funciones de red [Windows para](/windows/desktop/WNet/windows-networking-functions) administrar las letras de unidad asignadas. Aunque las funciones de WNet pueden devolverse correctamente, el comportamiento resultante no es el previsto. Cuando el sistema establece una unidad redirigida, se almacena por usuario. Solo el usuario puede administrar la unidad redirigida. El sistema realiza un seguimiento de las unidades redirigidas en función del identificador de seguridad de inicio de sesión (SID) del usuario. El SID de inicio de sesión es un identificador único para la sesión de inicio de sesión del usuario. Un solo usuario puede tener varias sesiones de inicio de sesión simultáneas en el sistema.

Si un servicio está configurado para ejecutarse con una cuenta de usuario, el sistema siempre crea una nueva sesión de inicio de sesión para el usuario e inicia el servicio en esa nueva sesión de inicio de sesión. Por lo tanto, un servicio no puede administrar las asignaciones de unidades establecidas dentro de las otras sesiones del usuario.

**Windows Server 2003:** En un equipo que tiene varias interfaces de red (es decir, un equipo de varios equipos), pueden producirse retrasos de hasta 60 segundos al usar rutas de acceso UNC para acceder a los archivos almacenados en un servidor de bloque de mensajes de servidor remoto (SMB). Para más información, consulte [el artículo 890553](https://support.microsoft.com/kb/890553) ayuda y soporte técnico Knowledge Base.

 

 
