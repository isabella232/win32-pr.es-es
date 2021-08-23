---
description: 'Más información sobre: Acerca de Extensible Storage Engine'
title: Acerca del motor Storage extensible
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 26a1d4d28f1d5957432202545ff94c4f18c37e5a521e0deadfdabfb72751adec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983875"
---
# <a name="about-extensible-storage-engine"></a>Acerca del motor Storage extensible


_**Se aplica a: Exchange Server** 2013 | Windows | Windows Servidor_

## <a name="about-extensible-storage-engine"></a>Acerca del motor Storage extensible

El motor de almacenamiento extensible (ESE) es un motor de base de datos que almacena información en una secuencia lógica. La información se puede recuperar secuencialmente o mediante el acceso a índices definidos. Las actualizaciones de la base de datos se implementan con una transacción para garantizar operaciones seguras. ESE permite el acceso simultáneo a varias bases de datos, incluidas las bases de datos de archivos de registro de transacciones que se pueden usar para la recuperación del sistema. ESE es escalable a aplicaciones grandes o pequeñas. Las siguientes características están disponibles con la interfaz de programación de aplicaciones (API) de ESE:

  - Copia de seguridad y restauración: una aplicación puede realizar copias coherentes del estado de datos mientras está en línea y modificando activamente el estado de los datos.

  - Navegación de cursor: la aplicación puede navegar con el cursor para acceder a los datos de forma secuencial o mediante índices.

  - Base de datos: colección de tablas de las que se hace una copia de seguridad y se restauran como una sola unidad.

  - Registro y recuperación de bloqueos: la API ese garantiza que se respeta la coherencia de los datos definidos por la aplicación incluso en caso de bloqueo del sistema.

  - Tablas: estructura fundamental de la base de datos ESE que se usa para almacenar datos.

  - Transacción: el motor de base de datos ESE proporciona transacciones durables aisladas coherentes atómicas (ACID) que permiten a las aplicaciones recuperar datos solo de estados de datos confiables y mantiene la coherencia de los datos en caso de una finalización inesperada del proceso o el apagado del sistema.

  - Escalable: la aplicación puede crear bases de datos de hasta 100 GB o de tan solo 1 MB.

