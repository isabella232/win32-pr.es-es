---
description: 'Cierta funcionalidad planeada para Windows Server 2003 de VSS no es totalmente compatible:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Restricciones en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7353b2d52a7222015f051e15ba07830b81d6aedda6323bca4378f459eb602ba8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124515"
---
# <a name="restrictions-in-windows-server-2003"></a>Restricciones en Windows Server 2003

Cierta funcionalidad planeada para Windows Server 2003 de VSS no es totalmente compatible:

-   Durante las operaciones de copia de seguridad, solo se permiten varias instancias de una clase de escritor determinada si solo una de esas instancias tiene un estado de restauración de escritor (vea [**VSS \_ WRITERRESTORE \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) que no sea VSS \_ WRE \_ NEVER. Si se cumple esta condición, todas las instancias de escritor participarán completamente durante la copia de seguridad, generando documentos de metadatos del escritor y participando en el control de eventos.
-   Durante las operaciones de restauración, solo un escritor recibirá los eventos de restauración generados por el solicitante. Si más de una instancia de una clase de escritor tiene un estado de restauración de escritor establecido en un valor distinto de VSS WRE NEVER, solo una instancia recibirá \_ \_ eventos de restauración. La instancia que los recibirá es indeterminada.

 

 



