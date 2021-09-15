---
description: 'Cierta funcionalidad planeada para Windows Server 2003 de VSS no es totalmente compatible:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Restricciones en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198e4ce79da4665bf712a64a466691041d452d86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474587"
---
# <a name="restrictions-in-windows-server-2003"></a>Restricciones en Windows Server 2003

Cierta funcionalidad planeada para Windows Server 2003 de VSS no es totalmente compatible:

-   Durante las operaciones de copia de seguridad, solo se permiten varias instancias de una clase de escritor determinada si solo una de esas instancias tiene un estado de restauración de escritor (vea [**VSS \_ WRITERRESTORE \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) que no sea VSS \_ WRE \_ NEVER. Si se cumple esta condición, todas las instancias de escritor participarán completamente durante la copia de seguridad, generando documentos de metadatos del escritor y participando en el control de eventos.
-   Durante las operaciones de restauración, solo un escritor recibirá los eventos de restauración generados por el solicitante. Si más de una instancia de una clase de escritor tiene un estado de restauración de escritor establecido en un valor distinto de VSS WRE NEVER, solo una instancia recibirá \_ \_ eventos de restauración. La instancia que los recibirá es indeterminada.

 

 



