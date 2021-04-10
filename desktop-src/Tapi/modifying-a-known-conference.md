---
description: En el fragmento de código siguiente se muestra la modificación de un intervalo de tiempo de conferencias. El intervalo de tiempo predeterminado es de treinta minutos. En este fragmento, el intervalo de tiempo se establece en un año.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modificación de una conferencia conocida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275173"
---
# <a name="modifying-a-known-conference"></a>Modificación de una conferencia conocida

\[Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

En el fragmento de código siguiente se muestra la modificación del intervalo de tiempo de una conferencia. El intervalo de tiempo predeterminado es de treinta minutos. En este fragmento, el intervalo de tiempo se establece en un año.

Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) y que se ha realizado una [enumeración de directorio de conferencia](enumerating-conference-directories.md) para obtener la entrada del directorio que se va a modificar.

Este fragmento también supone que no se trata de una conferencia de multidifusión. El cambio de las horas de una conferencia de multidifusión requiere la notificación del servidor de asignación de direcciones de multidifusión. Vea [adquirir una dirección de multidifusión](acquiring-a-multicast-address.md) para obtener un ejemplo de cómo trabajar con el direccionamiento multidifusión.


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



