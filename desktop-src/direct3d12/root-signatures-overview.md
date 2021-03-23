---
title: Introducción a las firmas raíz
description: La aplicación y los vínculos muestran las listas de comandos a los recursos que requieren los sombreadores.
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549139"
---
# <a name="root-signatures-overview"></a>Introducción a las firmas raíz

La aplicación y los vínculos muestran las listas de comandos a los recursos que requieren los sombreadores. La lista de comandos gráficos tiene un gráfico y una firma de raíz de proceso. Una lista de comandos de proceso simplemente tendrá una firma de raíz de proceso. Estas firmas raíz son independientes entre sí.

-   [Parámetros y argumentos raíz](#root-parameters-and-arguments)
-   [Constantes, descriptores y tablas raíz](#root-constants-descriptors-and-tables)
-   [Temas relacionados](#related-topics)

## <a name="root-parameters-and-arguments"></a>Parámetros y argumentos raíz

Una **firma raíz** es similar a una firma de función de la API, determina los tipos de datos que los sombreadores deberían esperar, pero no define la memoria o los datos reales. Un **parámetro raíz** es una entrada en la firma raíz. Los valores reales de los parámetros raíz establecidos y modificados en tiempo de ejecución se denominan **argumentos raíz**. Al cambiar los argumentos raíz se cambian los datos que los sombreadores leen.

## <a name="root-constants-descriptors-and-tables"></a>Constantes, descriptores y tablas raíz

La firma raíz puede contener tres tipos de parámetros: constantes de raíz (constantes insertadas en los argumentos raíz), descriptores de raíz (descriptores insertados en los argumentos raíz) y tablas de descriptores (punteros a un intervalo de descriptores en el montón de descriptores).

Las constantes raíz son valores de 32 bits en línea que se muestran en el sombreador como un búfer de constantes.

Los descriptores de raíz insertados deben contener descriptores a los que se accede con mayor frecuencia, aunque se limita a CBVs, y búferes UAV o SRV sin procesar o estructurados. Un tipo más complejo, como un SRV de textura de 2D, no se puede usar como un descriptor raíz. Los descriptores raíz no incluyen un límite de tamaño, por lo que no puede haber comprobaciones fuera de límite, a diferencia de los descriptores de los montones de descriptores, que incluyen un tamaño.

Las entradas de la tabla de descriptores en las signaturas raíz contienen el descriptor, el nombre de enlace del sombreador HLSL y la marca de visibilidad. Consulte [modelo de sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) para más información sobre los nombres de los sombreadores. En algunos requisitos de hardware, puede haber una mejora en el rendimiento, ya que solo los descriptores son visibles para las fases del sombreador que los requieren (consulte la [**\_ \_ visibilidad del sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)).

![entrada de tabla de descriptores raíz](images/root-descriptor-table.png)

El diseño de la firma raíz es bastante flexible, con algunas restricciones impuestas en hardware menos compatible. Independientemente del nivel de hardware, las aplicaciones siempre deben intentar crear la firma raíz tan pequeña como sea necesario para obtener la máxima eficacia. Las aplicaciones pueden componerse al tener más tablas de descriptores en la firma raíz pero menos espacio para las constantes raíz, o viceversa.

El contenido de la firma raíz (las tablas de descriptores, las constantes raíz y los descriptores raíz) que la aplicación ha enlazado automáticamente obtiene las versiones del controlador D3D12 siempre que cualquier parte del contenido cambie entre las llamadas a Draw (Graphics)/dispatch (Compute). Por lo tanto, cada Draw/Dispatch obtiene un conjunto completo único de estado de firma raíz.

Idealmente, hay grupos de objetos de estado de canalización (PSO) que comparten la misma firma raíz. Después de establecer una firma raíz en la canalización, todos los enlaces que define (descriptor tables, descriptores, constantes) se pueden establecer o cambiar individualmente, incluida la herencia en paquetes.

Una aplicación puede hacer su propio equilibrio entre el número de tablas de descriptores que quiere que los descriptores en línea (que ocupan más espacio pero quitar un direccionamiento indirecto) dejen constantes insertadas (que no tienen direccionamiento indirecto) que deseen en la firma raíz. Las aplicaciones deben usar la firma raíz de la manera más moderada posible, confiando en la memoria controlada por la aplicación, como los montones y los montones de descriptor que apuntan a ellos para representar los datos masivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 