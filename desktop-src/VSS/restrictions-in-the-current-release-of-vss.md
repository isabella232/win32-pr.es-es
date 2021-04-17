---
description: 'Determinada funcionalidad planeada para la versión 2003 de Windows Server de VSS no es totalmente compatible:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Restricciones en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198e4ce79da4665bf712a64a466691041d452d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696975"
---
# <a name="restrictions-in-windows-server-2003"></a>Restricciones en Windows Server 2003

Determinada funcionalidad planeada para la versión 2003 de Windows Server de VSS no es totalmente compatible:

-   Durante las operaciones de copia de seguridad, solo se permiten varias instancias de una clase de escritor determinada si solo una de esas instancias tiene un estado de restauración de escritor (consulte la [**\_ \_ enumeración WRITERRESTORE de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) distinto de VSS \_ WRE \_ Never. Si se cumple esta condición, todas las instancias del escritor participarán íntegramente durante la copia de seguridad, generando documentos de metadatos del escritor y participando en el control de eventos.
-   Durante las operaciones de restauración, solo un escritor recibirá eventos de restauración generados por el solicitante. Si más de una instancia de una clase del escritor tiene un estado de restauración del escritor establecido en un valor distinto de VSS \_ WRE \_ nunca, solo una instancia recibirá eventos de restauración. La instancia que las recibirá es indeterminada.

 

 



