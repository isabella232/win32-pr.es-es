---
description: La capa de datos suele contener información más estática&\# 8212; información conservada en un medio duradero.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimizar las llamadas entre la lógica de negocios y los datos de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705300"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de datos

La capa de datos suele contener información más estática: información conservada en un medio duradero. Dado que este nivel engloba información que es principalmente estática, requiere un análisis exhaustivo de los posibles cuellos de botella. Además de la posibilidad obvia de los cuellos de botella de conexión, las zonas activas pueden estar causadas por registros de acceso frecuente, métodos de acceso a datos ineficaces y la necesidad de coordinar el acceso a los sistemas heredados.

## <a name="connecting-to-the-data-tier"></a>Conexión a la capa de datos

Dos consideraciones desempeñan un papel importante en el diseño de una capa de datos para una aplicación COM+: la agrupación de conexiones y la [activación Just-in-Time (JIT) de com+](com--just-in-time-activation.md)y el uso de DSN. Los componentes que realizan conexiones con la capa de datos deben usar la [agrupación de objetos com+](com--object-pooling.md) establecida en el componente.

Al crear los DSN, use las cadenas del constructor de objetos especificadas en el componente en lugar de crear un DSN de archivo. Los DSN de archivo son más lentos que una conexión mediante una cadena de constructor de objeto. Las cadenas del constructor de objetos se pueden especificar en la hoja de propiedades del componente. Para obtener más información, vea [cadenas del constructor de objetos com+](com--object-constructor-strings.md).

Si usa componentes para tener acceso a una base de datos de SQL Server, utilice la agrupación de objetos COM+ en lugar de la agrupación de conexiones de SQL.

Si el componente usa ADO para capturar varios conjuntos de registros, establezca varias conexiones para el componente. Cuando ADO Recupera varios conjuntos de registros, crea varias conexiones en segundo plano si no se crean. Si los crea, puede agruparlos y tener más control sobre el número de conexiones utilizadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de presentación](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



