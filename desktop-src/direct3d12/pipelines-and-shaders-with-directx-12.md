---
title: Canalizaciones y sombreadores con Direct3D 12
description: La canalización programable de Direct3D 12 aumenta significativamente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd4ab60573fca9b9dce6759b5f87969199f83aed08aaa44a01f1501c402080e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952939"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Canalizaciones y sombreadores con Direct3D 12

La canalización programable de Direct3D 12 aumenta significativamente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior.

-   [Canalización de gráficos de Direct3D 12](#direct3d-12-graphics-pipeline)
-   [Objetos de estado de canalización](#pipeline-state-objects)
-   [Canalización de proceso de Direct3D 12](#direct3d-12-compute-pipeline)
-   [Temas relacionados](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Canalización de gráficos de Direct3D 12

En el diagrama siguiente se muestra el estado y la canalización de gráficos de Direct3D 12.

![diagrama que ilustra la canalización y el estado de Direct3d 12](images/pipeline.png)

Una canalización de gráficos es el flujo secuencial de entradas y salidas de datos a medida que la GPU representa fotogramas. Dado el estado y las entradas de la canalización, la GPU realiza una serie de operaciones para crear las imágenes resultantes. Una canalización de gráficos contiene sombreadores, que realizan cálculos y efectos de representación programables, y operaciones de función fija.

Tenga en cuenta lo siguiente al hacer referencia al diagrama de estado de canalización:

-   Las tablas de descriptores y los montones se pueden organizar arbitrariamente: se puede hacer referencia a los SRV, CBV y UAV y asignarse en cualquier orden.
-   Algunas operaciones de la canalización son configurables. Por ejemplo, la fusión de salida normalmente funciona en una base de lectura,modificación y escritura con las vistas de galería de símbolos de profundidad y destino de representación. Sin embargo, la canalización se puede configurar para que cualquiera de estas vistas sea de solo lectura o de solo escritura.
-   Los muestreadores estáticos no forman parte de los argumentos raíz, ya que son estáticos.

## <a name="pipeline-state-objects"></a>Objetos de estado de canalización

Direct3D 12 presenta el objeto de estado de canalización (PSO). En lugar de almacenar y representar el estado de la canalización en un gran número de objetos de alto nivel, los estados de los componentes de canalización como el ensamblador de entrada, el rasterizador, el sombreador de píxeles y la fusión de salida se almacenan en un PSO. Un PSO es un objeto de estado de canalización unificado que es inmutable después de la creación. El PSO seleccionado actualmente se puede cambiar de forma rápida y dinámica, y el hardware y los controladores pueden convertir directamente un PSO en instrucciones y estado de hardware nativos, y preparar la GPU para el procesamiento de gráficos. Para aplicar un PSO, el hardware copia una cantidad mínima de estado calculado previamente directamente en los registros de hardware. Esto elimina la sobrecarga causada por el controlador de gráficos y vuelve a calcular continuamente el estado de hardware en función de todas las configuraciones de canalización y representación aplicables actualmente. El resultado es una sobrecarga de llamada a draw significativamente reducida, un mayor rendimiento y más llamadas a draw por fotograma.

El PSO aplicado actualmente define y conecta todos los sombreadores que se usan en la canalización de representación. [El Lenguaje de sombreador de alto nivel (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) de Microsoft se compila previamente en objetos de sombreador, que luego se usan en tiempo de ejecución como entrada para los objetos de estado de canalización. Para obtener más información sobre cómo funciona el PSO dentro de la canalización de gráficos, vea Administración del estado de canalización [de gráficos en Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

## <a name="direct3d-12-compute-pipeline"></a>Canalización de proceso de Direct3D 12

En el diagrama siguiente se muestra el estado y la canalización de proceso de Direct3D 12.

![Diagrama que muestra la canalización de proceso de Direct3D 12.](images/compute-pipeline.png)

No hay unidades de función fijas en esta canalización, pero los montones de descriptores, los montones de muestreador y los muestreadores estáticos siguen estando disponibles en el proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 