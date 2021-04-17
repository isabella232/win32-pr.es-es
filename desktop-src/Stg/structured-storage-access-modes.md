---
title: Modos de acceso de almacenamiento estructurado
description: Los mecanismos para controlar el acceso simultáneo a un objeto, por parte de varios procesos y usuarios, son esenciales.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Almacenamiento estructurado Strctd STG, Fundamentals, funciones de API, marcas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665597"
---
# <a name="structured-storage-access-modes"></a>Modos de acceso de almacenamiento estructurado

Los mecanismos para controlar el acceso simultáneo a un objeto, por parte de varios procesos y usuarios, son esenciales. COM proporciona estos mecanismos definiendo modos de acceso para los objetos de almacenamiento y de secuencia. Los elementos secundarios heredan el modo de acceso especificado para un objeto de almacenamiento primario, aunque se pueden colocar restricciones adicionales en el almacenamiento o la secuencia secundaria. Un objeto de flujo o almacenamiento anidado se puede abrir en el mismo modo o en un modo más restringido que el de su elemento primario, pero no se puede abrir en un modo menos restringido que el de su elemento primario.

Los modos de acceso se especifican mediante los valores enumerados en [**constantes de STGM**](stgm-constants.md). Estos valores sirven como marcas para pasar como argumentos a métodos en la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y las funciones de API asociadas. Normalmente, se combinan varias marcas en el parámetro *grfMode*, mediante una operación **or** booleana.

Las marcas se dividen en seis grupos. Solo se puede especificar una marca de cada grupo a la vez:

-   [Marcas de transacción](transaction-flags.md)
-   [Marcas de creación de almacenamiento](storage-creation-flags.md)
-   [Marcas de creación temporales](temporary-creation-flags.md)
-   [Marcas de prioridad](priority-flags.md)
-   [Marcas de permisos de acceso](access-permission-flags.md)
-   [Marcas de acceso compartido](shared-access-flags.md)

 

 




