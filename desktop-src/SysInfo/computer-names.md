---
description: Los nombres DNS se componen de uno o varios componentes separados por un punto (por ejemplo, msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Nombres de equipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf076f42e3353aa03db951e9dec428766cf4895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913845"
---
# <a name="computer-names"></a>Nombres de equipos

Los nombres DNS se componen de uno o varios componentes separados por un punto (por ejemplo, msdn.microsoft.com). Cada componente puede tener hasta 63 bytes. Cada nombre puede tener hasta 255 bytes en total. Los nombres DNS se representan en el juego de caracteres UTF-8 o Unicode. El nombre no distingue entre mayúsculas y minúsculas. Para obtener más información, vea [**DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Un equipo se identifica de forma exclusiva por su nombre DNS completo, que consta de su nombre de host DNS y el nombre del dominio DNS al que está asignado. Para recuperar el nombre DNS completo de un equipo, el nombre de host DNS o el nombre de dominio DNS, llame a la función [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) . Para establecer el nombre de host DNS o el nombre de dominio DNS de un equipo, llame a la función [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) . Los cambios de nombre no surtirán efecto hasta que el usuario reinicie el equipo.

Los nombres NetBIOS constan de hasta 15 bytes de caracteres OEM, como letras, dígitos, guiones y puntos. Algunos caracteres son específicos del juego de caracteres. Los nombres NetBIOS se representan normalmente en el juego de caracteres OEM. El juego de caracteres OEM depende de la configuración regional. Algunos juegos de caracteres OEM representan ciertos caracteres como dos bytes. Los nombres NetBIOS, por Convención, se representan en mayúsculas, donde el algoritmo de conversión de minúsculas a mayúsculas es dependiente del juego de caracteres OEM.

Las funciones [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) y [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) también pueden establecer y recuperar el nombre NetBIOS del equipo. Por Convención, el nombre NetBIOS y el nombre de host DNS son interdependientes. Cuando se modifica el nombre DNS, el nombre NetBIOS también se actualiza. El nombre NetBIOS es la representación OEM del nombre de host DNS con un máximo \_ de \_ caracteres de longitud de COMPUTERNAME. Si establece un nombre de host DNS de más de \_ \_ los caracteres de longitud máximo COMPUTERNAME, el nombre NetBIOS se establece en una versión truncada del nombre de host DNS. De lo contrario, el nombre de host DNS completo se convierte en el nombre NetBIOS de OEM. ADVERTENCIA: Si modifica el nombre de NetBIOS para que no sea una asignación truncada del nombre DNS, se interrumpirán las aplicaciones que usan funciones como [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) que se basan en esta Convención.

 

 
