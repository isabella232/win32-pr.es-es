---
title: Canalizaciones y sombreadores con Direct3D 12
description: La canalización programable de Direct3D 12 aumenta considerablemente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104549103"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Canalizaciones y sombreadores con Direct3D 12

La canalización programable de Direct3D 12 aumenta considerablemente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior.

-   [Canalización de gráficos de Direct3D 12](#direct3d-12-graphics-pipeline)
-   [Objetos de estado de canalización](#pipeline-state-objects)
-   [Canalización de proceso de Direct3D 12](#direct3d-12-compute-pipeline)
-   [Temas relacionados](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Canalización de gráficos de Direct3D 12

En el diagrama siguiente se muestra el estado y la canalización de gráficos de Direct3D 12.

![diagrama que ilustra el estado y la canalización de Direct3D 12](images/pipeline.png)

Una canalización de gráficos es el flujo secuencial de entradas y salidas de datos a medida que la GPU representa los fotogramas. Dado el estado y las entradas de la canalización, la GPU realiza una serie de operaciones para crear las imágenes resultantes. Una canalización de gráficos contiene sombreadores, que realizan cálculos y efectos de representación programables, y operaciones de función fijas.

Tenga en cuenta lo siguiente al hacer referencia al diagrama de estado de la canalización:

-   Las tablas y los montones de descriptores se pueden organizar arbitrariamente: se puede hacer referencia a SRVs, CBVs y UAVs y se pueden asignar en cualquier orden.
-   Algunas operaciones de la canalización son configurables. Por ejemplo, la fusión de salida actúa normalmente en una base de lectura-modificación y escritura con las vistas de estarcido de profundidad y de destino de representación. Sin embargo, se puede configurar la canalización para que cualquiera de estas vistas sea de solo lectura o de solo escritura.
-   Los muestreadores estáticos no forman parte de los argumentos raíz, ya que son estáticos.

## <a name="pipeline-state-objects"></a>Objetos de estado de canalización

Direct3D 12 presenta el objeto de estado de canalización (PSO). En lugar de almacenar y representar el estado de canalización en un gran número de objetos de alto nivel, los Estados de los componentes de canalización como el ensamblador de entrada, el rasterizador, el sombreador de píxeles y la fusión de salida se almacenan en un PSO. Un PSO es un objeto de estado de canalización unificado que es inmutable después de la creación. Actualmente se puede cambiar el PSO seleccionado de forma rápida y dinámica, y el hardware y los controladores pueden convertir directamente un PSO en instrucciones y Estados de hardware nativo y preparar la GPU para el procesamiento de gráficos. Para aplicar un PSO, el hardware copia una cantidad mínima de estado calculado previamente directamente en los registros de hardware. Esto elimina la sobrecarga causada por que el controlador de gráficos recalcule continuamente el estado del hardware en función de todas las opciones de representación y de canalización aplicables actualmente. El resultado se reduce significativamente la sobrecarga de la llamada a Draw, el aumento del rendimiento y más llamadas a Draw por fotograma.

El PSO aplicado actualmente define y conecta todos los sombreadores que se usan en la canalización de representación. El [lenguaje HLSL (Microsoft High Level Shader Language)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) se compila previamente en objetos de sombreador que, a continuación, se usan en tiempo de ejecución como entrada para los objetos de estado de canalización. Para obtener más información sobre cómo funciona el PSO dentro de la canalización de gráficos, vea [administrar el estado de canalización de gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="direct3d-12-compute-pipeline"></a>Canalización de proceso de Direct3D 12

En el diagrama siguiente se ilustra el estado y la canalización de proceso de Direct3D 12.

![Diagrama que muestra la canalización de proceso de Direct3D 12.](images/compute-pipeline.png)

No hay unidades de función fijas en esta canalización; sin embargo, los montones de descriptores, los montones de muestra y los muestreadores estáticos siguen estando disponibles en Compute.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 