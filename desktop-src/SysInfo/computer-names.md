---
description: Los nombres DNS constan de uno o varios componentes separados por un punto (por ejemplo, msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Nombres de equipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8687d6d510247a2bbb2850e6a668a63f0108b2bc344ed161cb73e28d2b47eeaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885795"
---
# <a name="computer-names"></a>Nombres de equipos

Los nombres DNS constan de uno o varios componentes separados por un punto (por ejemplo, msdn.microsoft.com). Cada componente puede tener hasta 63 bytes. Cada nombre puede tener un total de hasta 255 bytes. Los nombres DNS se representan en el juego de caracteres UTF-8 o Unicode. El nombre no distingue entre mayúsculas y minúsculas. Para obtener más información, [**vea DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Un equipo se identifica de forma única por su nombre DNS completo, que consta de su nombre de host DNS y el nombre del dominio DNS al que está asignado. Para recuperar el nombre DNS completo, el nombre de host DNS o el nombre de dominio DNS de un equipo, llame a la [**función GetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) Para establecer el nombre de host DNS o el nombre de dominio DNS de un equipo, llame a la [**función SetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) Los cambios de nombre no tienen efecto hasta que el usuario reinicia el equipo.

Los nombres NetBIOS constan de hasta 15 bytes de caracteres OEM, incluidas letras, dígitos, guiones y puntos. Algunos caracteres son específicos del juego de caracteres. Los nombres NetBIOS se representan normalmente en el juego de caracteres oem. El juego de caracteres oem depende de la configuración regional. Algunos juegos de caracteres OEM representan determinados caracteres como dos bytes. Los nombres NetBIOS, por convención, se representan en mayúsculas, donde el algoritmo de traducción de minúsculas a mayúsculas depende del juego de caracteres oem.

Las [**funciones SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) y [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) también pueden establecer y recuperar el nombre NetBIOS del equipo. Por convención, el nombre NetBIOS y el nombre de host DNS son interdependientes. Al modificar el nombre DNS, también se actualiza el nombre NetBIOS. El nombre NetBIOS es la representación oem del nombre de host DNS hasta un máximo \_ de caracteres COMPUTERNAME \_ LENGTH. Si establece un nombre de host DNS de más de un máximo de caracteres COMPUTERNAME LENGTH, el nombre NetBIOS se establece en una versión truncada del \_ nombre de host \_ DNS. De lo contrario, el nombre de host DNS completo se traduce en el nombre NetBIOS de OEM. Advertencia: Si modifica el nombre NetBIOS para que no sea una asignación truncada del nombre DNS, interrumpirá las aplicaciones que usan funciones como [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) que se basan en esta convención.

 

 
