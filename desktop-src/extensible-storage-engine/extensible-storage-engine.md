---
description: 'Más información sobre: Motor de Storage extensible'
title: Motor de Storage extensible
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: d1ec139cf947cb2d95bfccf3737c1f6559bf01ffbfa55f2e9a7d1e890efd6a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980825"
---
# <a name="extensible-storage-engine"></a>Motor de Storage extensible


_**Se aplica a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine"></a>Motor de Storage extensible

Extensible Storage Engine (ESE) es una tecnología avanzada de almacenamiento de método de acceso indexado y secuencial (ISAM). ESE permite a las aplicaciones almacenar y recuperar datos de tablas mediante la navegación de cursor indexada o secuencial. Admite esquemas desnormalizados, incluidas tablas anchas con numerosas columnas dispersas, columnas con varios valores e índices dispersos y enriquecidos. Permite a las aplicaciones disfrutar de un estado de datos coherente mediante la actualización y recuperación de datos con transacciones. Se proporciona un mecanismo de recuperación de bloqueos para que la coherencia de los datos se mantenga incluso en caso de bloqueo del sistema. Proporciona transacciones ACID (Atomic Consistent Isolated Durable) a través de datos y esquemas mediante un registro de escritura por adelantado y un modelo de aislamiento de instantáneas. Las transacciones en ESE son muy simultáneas, lo que hace que ese sea útil para las aplicaciones de servidor. Almacena en caché los datos para maximizar el acceso de alto rendimiento a los datos. Además, es ligero, lo que lo hace útil para las aplicaciones que sirven en roles auxiliares.

ESE se usa en aplicaciones que requieren almacenamiento de datos estructurados rápidos o ligeros, donde el acceso a archivos sin procesar o el registro no admiten los requisitos de indexación o tamaño de datos de la aplicación.

Lo usan las aplicaciones que nunca almacenan más de 1 megabyte de datos y se ha usado en aplicaciones con bases de datos en casos extremos superiores a 1 terabyte y normalmente más de 50 gigabytes.

Esta documentación está pensada para desarrolladores que están familiarizados con C y C++, y conceptos básicos de base de datos como tablas, columnas, índices, recuperación y transacciones. El único método de acceso para ESE es la API de C que se describe en esta documentación.

El motor Storage extensible es un componente Windows que se introdujo en Windows 2000. No todas las características o API están disponibles en todas las versiones de Windows sistemas operativos.

ESE proporciona un motor de almacenamiento en modo de usuario que administra los datos dentro de archivos binarios planos a los que se puede acceder a través de Windows API. Se accede a ESE a través de un archivo DLL que se carga directamente en el proceso de la aplicación. el propio motor de base de datos no requiere ni proporciona ningún método de acceso remoto. Aunque ESE no tiene ningún método de acceso remoto o entre procesos, los archivos de datos que usa se pueden proporcionar de forma remota mediante el bloque de mensajes del servidor (SMB) a través de las API de Windows, pero esto no se recomienda.

**Tenga** Windows xp de 64 bits edition es igual que Windows Server 2003 con el fin de determinar el conjunto de características de ESE que se admite.  

### <a name="notes"></a>Notas

ESE se conocía anteriormente como Joint Engine Technology (JET) Blue y, con frecuencia, el término "JET Blue" o "JET" se usa indistintamente con el término ESE fuera de esta documentación. Sin embargo, de hecho hay dos implementaciones completamente independientes de la API de JET, denominadas JET Blue y JET Red. El término "JET" también se usa con frecuencia para hacer referencia a JET Red, que es el motor de base de datos que se usa con Microsoft Office Access. Las dos implementaciones de JET son completamente diferentes, se mantienen por separado, tienen un conjunto de características muy diferente y no son intercambiables. En la documentación de ESE, "JET" hace referencia a ese o a la API de JET a medida que ese lo implementa. Todas las referencias a JET Red siempre se etiquetarán explícitamente como "JET Red".

### <a name="in-this-section"></a>En esta sección

[Referencia del motor Storage extensible](./extensible-storage-engine-reference.md)
