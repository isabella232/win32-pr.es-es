---
description: 'Más información acerca de: motor de almacenamiento extensible'
title: Motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0ef85de696f52d2220c11b05ed7ada76a70df871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082305"
---
# <a name="extensible-storage-engine"></a>Motor de almacenamiento extensible


_**Se aplica a:** Windows | Windows Server_

## <a name="extensible-storage-engine"></a>Motor de almacenamiento extensible

El motor de almacenamiento extensible (ESE) es una tecnología de almacenamiento avanzada indizada y de método de acceso secuencial (ISAM). ESE permite que las aplicaciones almacenen y recuperen datos de tablas mediante la navegación de cursor secuencial o indizada. Admite esquemas desnormalizados, como tablas anchas con numerosas columnas dispersas, columnas con varios valores, y índices dispersos y enriquecidos. Permite a las aplicaciones disfrutar de un estado de datos coherente mediante la actualización y la recuperación de datos de transacción. Se proporciona un mecanismo de recuperación de bloqueos para mantener la coherencia de los datos incluso en caso de que se produzca un bloqueo del sistema. Proporciona transacciones ACID (duraderos aisladas atómicas) sobre los datos y el esquema mediante un registro de escritura previa y un modelo de aislamiento de instantánea. Las transacciones de ESE son muy simultáneas y hacen que ESE sea útil para las aplicaciones de servidor. Almacena en memoria caché los datos para maximizar el acceso de alto rendimiento a los datos. Además, es ligero, lo que resulta útil para las aplicaciones que sirven en roles auxiliares.

ESE es para su uso en aplicaciones que requieren un almacenamiento de datos estructurado rápido o ligero, donde el acceso a archivos sin formato o el registro no admiten los requisitos de tamaño de datos o de indización de la aplicación.

Lo usan las aplicaciones que nunca almacenan más de 1 megabyte de datos y se ha usado en aplicaciones con bases de datos en casos extremos con un exceso de 1 terabyte y, por lo general, más de 50 gigabytes.

Esta documentación está destinada a desarrolladores que están familiarizados con C y C++, y conceptos básicos de bases de datos como tablas, columnas, índices, recuperación y transacciones. El único método de acceso para ESE es la API de C que se describe en esta documentación.

El motor de almacenamiento extensible es un componente de Windows que se presentó en Windows 2000. No todas las características o API están disponibles en todas las versiones de los sistemas operativos Windows.

ESE proporciona un motor de almacenamiento de modo de usuario que administra datos dentro de archivos binarios y sin formato a los que se puede tener acceso a través de las API de Windows. Se tiene acceso a ESE a través de un archivo DLL que se carga directamente en el proceso de la aplicación. no se necesita ningún método de acceso remoto o lo proporciona el propio motor de base de datos. Aunque ESE no tiene ningún método de acceso remoto o entre procesos, los archivos de datos que usa se pueden proporcionar de forma remota mediante el bloque de mensajes del servidor (SMB) a través de las API de Windows, pero no se recomienda hacerlo.

**Nota:**  Windows XP 64-bit Edition es igual que Windows Server 2003 con el fin de determinar el conjunto de características de ESE que se admite.

### <a name="notes"></a>Notas

ESE antes se conocía como tecnología de motor conjunto (JET) Blue, por lo que con frecuencia el término "JET Blue" o "JET" se usa indistintamente con el término ESE fuera de esta documentación. Sin embargo, en realidad hay dos implementaciones completamente independientes de la API de JET, llamadas JET Blue y JET red. El término "JET" también se usa con frecuencia para hacer referencia a JET red, que es el motor de base de datos que se usa con Microsoft Office acceso. Las dos implementaciones de JET son completamente diferentes, se mantienen por separado, tienen un conjunto de características enormemente diferente y no son intercambiables. En la documentación de ESE, "JET" hace referencia a ESE o a la API de JET, ya que ESE lo implementa. Todas las referencias a la red de JET siempre se etiquetarán explícitamente como "JET red".

### <a name="in-this-section"></a>En esta sección

[Referencia del motor de almacenamiento extensible](./extensible-storage-engine-reference.md)
