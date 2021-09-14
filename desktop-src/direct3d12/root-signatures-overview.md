---
title: Introducción a las firmas raíz
description: La aplicación configura una firma raíz y vincula las listas de comandos a los recursos que requieren los sombreadores.
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072884"
---
# <a name="root-signatures-overview"></a>Introducción a las firmas raíz

La aplicación configura una firma raíz y vincula las listas de comandos a los recursos que requieren los sombreadores. La lista de comandos de gráficos tiene una firma raíz de proceso y gráficos. Una lista de comandos de proceso simplemente tendrá una firma raíz de proceso. Estas firmas raíz son independientes entre sí.

-   [Parámetros y argumentos raíz](#root-parameters-and-arguments)
-   [Constantes, descriptores y tablas raíz](#root-constants-descriptors-and-tables)
-   [Temas relacionados](#related-topics)

## <a name="root-parameters-and-arguments"></a>Parámetros y argumentos raíz

Una **firma raíz** es similar a una firma de función de API, determina los tipos de datos que deben esperar los sombreadores, pero no define la memoria o los datos reales. Un **parámetro raíz** es una entrada de la firma raíz. Los valores reales de los parámetros raíz establecidos y modificados en tiempo de ejecución se **denominan argumentos raíz**. Al cambiar los argumentos raíz, se cambian los datos que los sombreadores leen.

## <a name="root-constants-descriptors-and-tables"></a>Constantes, descriptores y tablas raíz

La firma raíz puede contener tres tipos de parámetros; constantes raíz (constantes incluidas en los argumentos raíz), descriptores raíz (descriptores incluidos en los argumentos raíz) y tablas de descriptores (punteros a un intervalo de descriptores en el montón de descriptores).

Las constantes raíz son valores de 32 bits en línea que se muestran en el sombreador como búfer constante.

Los descriptores raíz inlined deben contener descriptores a los que se accede con más frecuencia, aunque se limita a CBV y búferes UAV o SRV sin formato o estructurados. Un tipo más complejo, como un SRV de textura 2D, no se puede usar como descriptor raíz. Los descriptores raíz no incluyen un límite de tamaño, por lo que no puede haber ninguna comprobación fuera de los límites, a diferencia de los descriptores de los montones de descriptores, que incluyen un tamaño.

Las entradas de tabla de descriptor dentro de las firmas raíz contienen el descriptor, el nombre de enlace del sombreador HLSL y la marca de visibilidad. Consulte [Shader Model 5.1 (Modelo de sombreador 5.1)](/windows/desktop/direct3dhlsl/shader-model-5-1) para obtener más información sobre los nombres de sombreador. En algún hardware, puede haber una ganancia de rendimiento al hacer que los descriptores sean visibles para las fases del sombreador que los requieran (consulte VISIBILIDAD DEL [**\_ SOMBREADOR \_ de D3D12).**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)

![entrada de tabla de descriptor raíz](images/root-descriptor-table.png)

El diseño de la firma raíz es bastante flexible, con algunas restricciones impuestas en hardware menos capaz. Independientemente del nivel de hardware, las aplicaciones siempre deben intentar que la firma raíz sea tan pequeña como sea necesario para lograr la máxima eficacia. Las aplicaciones pueden no tener más tablas de descriptores en la firma raíz, pero menos espacio para las constantes raíz, o viceversa.

El contenido de la firma raíz (las tablas de descriptores, las constantes raíz y los descriptores raíz) que la aplicación ha enlazado obtiene automáticamente versiones del controlador D3D12 cada vez que cualquier parte del contenido cambia entre llamadas a draw (gráficos)/dispatch (proceso). Por lo tanto, cada draw/dispatch obtiene un conjunto completo único de estado de firma raíz.

Lo ideal es que haya grupos de objetos de estado de canalización (PSO) que compartan la misma firma raíz. Una vez establecida una firma raíz en la canalización, todos los enlaces que define (tablas de descriptores, descriptores, constantes) se pueden establecer o cambiar individualmente, incluida la herencia en agrupaciones.

Una aplicación puede hacer su propio equilibrio entre el número de tablas de descriptores que desea que los descriptores en línea de los verse (que necesitan más espacio, pero quitan un direccionamiento indirecto) de las constantes insertas (que no tienen ningún direccionamiento indirecto) que desean en la firma raíz. Las aplicaciones deben usar la firma raíz con la mayor moderación posible, basándose en la memoria controlada por la aplicación, como montones y montones de descriptores que apuntan a ellos para representar datos masivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 