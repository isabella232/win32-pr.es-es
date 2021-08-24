---
description: El fragmento de código siguiente muestra la modificación de un intervalo de tiempo de conferencias. El intervalo de tiempo predeterminado es de treinta minutos. En este fragmento, el intervalo de tiempo se establece en un año.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modificar una conferencia conocida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b139b05f70f801a28b91ecb6c2773fd740f10df7c0fd2b8e86b904b210cc50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575605"
---
# <a name="modifying-a-known-conference"></a>Modificar una conferencia conocida

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El fragmento de código siguiente muestra la modificación del intervalo de tiempo de una conferencia. El intervalo de tiempo predeterminado es de treinta minutos. En este fragmento, el intervalo de tiempo se establece en un año.

En este fragmento se supone que ya se ha realizado la conexión [a](enumerating-conference-directories.md) un [servidor ILS](connecting-to-an-ils-server.md) y que se ha realizado una enumeración de directorio de conferencia para obtener la entrada de directorio que se modificará.

En este fragmento también se da por supuesto que no se trata de una conferencia de multidifusión. Cambiar las horas de una conferencia de multidifusión requiere la notificación del servidor de asignación de direcciones de multidifusión. Consulte [Adquisición de una dirección de multidifusión](acquiring-a-multicast-address.md) para obtener un ejemplo de cómo trabajar con direccionamiento de multidifusión.


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



