---
description: 'Más información acerca de: acerca del motor de almacenamiento extensible'
title: Acerca del motor de almacenamiento extensible
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000880"
---
# <a name="about-extensible-storage-engine"></a>Acerca del motor de almacenamiento extensible


_**Se aplica a:** Exchange Server 2013 | Windows | Windows Server_

## <a name="about-extensible-storage-engine"></a>Acerca del motor de almacenamiento extensible

El motor de almacenamiento extensible (ESE) es un motor de base de datos que almacena información en una secuencia lógica. La información se puede recuperar de forma secuencial o mediante el acceso a índices definidos. Las actualizaciones de la base de datos se implementan con una transacción con el fin de garantizar operaciones seguras. ESE permite el acceso simultáneo a varias bases de datos, incluidas las bases de datos de archivos de registro de transacciones que se pueden utilizar para la recuperación del sistema. ESE es escalable a aplicaciones grandes o pequeñas. Las siguientes características están disponibles con la interfaz de programación de aplicaciones (API) de ESE:

  - Copias de seguridad y restauración: una aplicación puede hacer copias coherentes del estado de los datos mientras está en línea y modificando activamente el estado de los datos.

  - Navegación por el cursor: la aplicación puede navegar con el cursor para tener acceso a los datos de forma secuencial o mediante índices.

  - Base de datos: colección de tablas de las que se realiza una copia de seguridad y se restaura como una sola unidad.

  - Registro y recuperación de bloqueos: la API de ESE garantiza que la coherencia de los datos definidos por la aplicación se respeta incluso en caso de que se produzca un bloqueo del sistema.

  - Tablas: estructura fundamental de la base de datos de ESE que se utiliza para almacenar los datos.

  - Transacción: el motor de base de datos ESE proporciona transacciones duraderas aisladas atómicas (ACID) que permiten a las aplicaciones recuperar datos únicamente de los Estados de datos confiables y mantiene la coherencia de los datos en caso de que se produzca una terminación de proceso inesperada o un cierre del sistema.

  - Escalable: la aplicación puede crear bases de datos de hasta 100 GB o tan pequeñas como 1 MB.

