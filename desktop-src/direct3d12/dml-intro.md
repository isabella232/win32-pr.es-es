---
title: Introducción a DirectML
description: Direct Machine Learning (DirectML) es una API de bajo nivel para machine learning (ML).
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 2dd37bc4c27364e26e4bbd4ae2cf5d43031c3314
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105111"
---
# <a name="introduction-to-directml"></a>Introducción a DirectML

## <a name="summary"></a>Resumen

Direct Machine Learning (DirectML) es una API de bajo nivel para machine learning (ML). Los primitivos de machine learning con aceleración de hardware (denominados operadores) son los bloques de creación de DirectML. A partir de estos bloques de creación, puede desarrollar dichas técnicas de aprendizaje automático como la escalabilidad, el suavizado de contorno y la transferencia de estilo, al nombre pero algunas. Denoising y la superresolución, por ejemplo, le permiten lograr efectos raytraced impresionantes con menos rayos por píxel.

Puede integrar las cargas de trabajo de inferencia del aprendizaje automático en su juego, motor, middleware, back-end u otra aplicación. DirectML tiene un flujo de trabajo y una interfaz de programación de estilo DirectX 12 (C++ nativo, nano-COM), y es compatible con todo el hardware compatible con DirectX 12. Para las aplicaciones de ejemplo de DirectML, incluido un ejemplo de una aplicación de DirectML mínima, vea [aplicaciones de ejemplo de DirectML](dml-min-app.md).

DirectML se ha introducido en Windows 10, versión 1903 y en la versión correspondiente de la Windows SDK.

## <a name="is-directml-appropriate-for-my-project"></a>¿Es DirectML adecuado para mi proyecto?

DirectML es un componente de la paraguas [machine learning Windows](/windows/ai) . La API WinML de nivel superior se centra principalmente en el modelo, con su flujo de trabajo de carga-enlace-evaluación. Pero los dominios como juegos y motores suelen necesitar un nivel inferior de abstracción y un mayor grado de control del desarrollador, con el fin de aprovechar al máximo el silicio. Si va a contar los milisegundos y se consuman los tiempos de fotogramas, DirectML satisfará sus necesidades de aprendizaje automático.

Para escenarios confiables en tiempo real, de alto rendimiento, de baja latencia y de restricción de recursos, use DirectML (en lugar de WinML). Puede integrar DirectML directamente en el motor o la canalización de representación existentes. O bien, en un nivel superior para los marcos de aprendizaje automático y el middleware personalizados, DirectML puede proporcionar un back-end de alto rendimiento en Windows.

WinML se implementa mediante DirectML como uno de sus back-ends.

## <a name="what-work-does-directml-do-and-what-work-must-i-do-as-the-developer"></a>Qué trabajo hace DirectML; ¿y qué trabajo *debo* hacer como desarrollador?

DirectML ejecuta de forma eficaz las capas individuales del modelo de inferencia en la GPU (o en núcleos de aceleración de AI, si existen). Cada capa es un operador y DirectML proporciona una biblioteca de operadores primitivos de aprendizaje automático de bajo nivel y acelerados por hardware. Estos operadores tienen optimizaciones específicas del hardware y específicas de la arquitectura diseñadas para ellos (más información sobre esto en la sección [¿por qué funciona DirectML?](#why-does-directml-perform-so-well)). Al mismo tiempo, como desarrollador, verá una única interfaz independiente del proveedor para ejecutar esos operadores.

La biblioteca de operadores de DirectML proporciona todas las operaciones habituales que se espera que puedan usarse en una carga de trabajo de machine learning.

- Operadores de activación, como **linear**, **ReLU**, **sigmoidea**, **tanh**, etc.
- Operadores de tipo elemento, como **Add**, **exp**, **log**, **Max**, **min**, **Sub** y more.
- Operadores de circunvolución, como la **circunvolución** 2D y 3D, etc.
- Operadores de reducción, como **argmin**, **Average**, **L2**, **SUM**, etc.
- Operadores de agrupación, como **Average**, **LP** y **Max**.
- Operadores de red neuronal (NN), como **GEMM**, **Gru**, **LSTM** y **RNN**.
- Y muchas más.

Para obtener el máximo rendimiento y no pagar por lo que no se usa, DirectML coloca el control en sus manos como desarrollador sobre cómo se ejecuta la carga de trabajo de machine learning en el hardware. Averiguar qué operadores deben ejecutarse y cuándo, es responsabilidad suya del desarrollador. Entre las tareas que se dejan a su discreción se incluyen: transcribir el modelo; simplificar y optimizar las capas; cargas de carga; asignación de recursos, enlace, administración de memoria (al igual que con Direct3D 12); y la ejecución del gráfico.

Puede conservar el conocimiento de alto nivel de los gráficos (puede codificar el modelo directamente o puede escribir su propio cargador de modelos). Puede diseñar un modelo de escalado, por ejemplo, mediante el uso de varias capas para cada uno de los operadores de **muestreo**, **convolución**, **normalización** y **activación** . Con esa familiaridad, la programación cuidadosa y la administración de barreras, puede extraer el mayor paralelismo y el rendimiento del hardware. Si va a desarrollar un juego, la administración y el control de recursos cuidadosos sobre la programación le permite intercalar cargas de trabajo de aprendizaje automático y trabajos de representación tradicionales para saturar la GPU.

## <a name="whats-the-high-level-directml-workflow"></a>¿Cuál es el flujo de trabajo de DirectML de alto nivel?

Esta es la receta de alto nivel sobre cómo esperamos que se use DirectML. En las dos fases principales de la inicialización y la ejecución, los trabajos se registran en las listas de comandos y, a continuación, se ejecutan en una cola.

### <a name="initialization"></a>Inicialización

1. Cree los recursos de Direct3D 12 &mdash; el dispositivo Direct3D 12, la cola de comandos, la lista de comandos y los recursos como los montones de descriptores.
2. Dado que está realizando la inferencia de aprendizaje automático, así como la carga de trabajo de representación, cree los recursos de DirectML en &mdash; el dispositivo DirectML y en las instancias de operador. Si tiene un modelo de aprendizaje automático en el que necesita realizar un tipo determinado de circunvolución con un tamaño determinado del filtro tensores con un tipo de datos determinado, todos ellos son todos los parámetros del operador de **convolución** de DirectML.
3. Los registros de DirectML funcionan en listas de comandos de Direct3D 12. Por lo tanto, una vez que se realiza la inicialización, se registra el enlace y la inicialización de (por ejemplo) el operador de circunvolución en la lista de comandos. A continuación, cierre y ejecute la lista de comandos en la cola como de costumbre.

### <a name="execution"></a>Ejecución

1. Cargue los diez pesos en los recursos. Un tensores de DirectML se representa mediante un recurso de Direct3D 12 normal. Por ejemplo, si desea cargar los datos de peso en la GPU, hágalo de la misma forma que lo haría con cualquier otro recurso de Direct3D 12 (use un montón de carga o la cola de copia).
2. A continuación, debe enlazar esos recursos de Direct3D 12 como los de entrada y salida. Grabe en la lista de comandos el enlace y la ejecución de los operadores.
3. Cierre y ejecute la lista de comandos.

Al igual que con Direct3D 12, la duración de los recursos y la sincronización son responsabilidad suya. Por ejemplo, no libere los objetos de DirectML al menos hasta que hayan finalizado la ejecución en la GPU.

## <a name="why-does-directml-perform-so-well"></a>¿Por qué DirectML funciona tan bien?

Hay una buena razón por la que no debe escribir su propio operador de convolución (por ejemplo,) como HLSL en un [sombreador de cálculo](/windows/desktop/direct3d12/pipelines-and-shaders-with-directx-12#direct3d-12-compute-pipeline). La ventaja de usar DirectML es que, &mdash; además de ahorrarle el esfuerzo de homebrewing su propia solución, &mdash; tiene la capacidad de ofrecer un rendimiento mucho mejor que el que podría lograr con un sombreador de cálculo de uso general y escrito para algo como **circunvolución** o **LSTM**.

DirectML logra esto en parte debido a la característica de metacomandos de Direct3D 12. Los metacomandos exponen un cuadro negro de funcionalidad hasta DirectML, lo que permite a los proveedores de hardware proporcionar acceso DirectML a las optimizaciones específicas del hardware del proveedor y específicas de la arquitectura. Varios operadores &mdash; por ejemplo, convolución seguido de &mdash; la activación se pueden *fusionar* mediante combinación en un solo metacomando. Debido a estos factores, DirectML tiene la capacidad de superar el rendimiento de incluso un sombreador de cálculo totalmente escrito y optimizado para ejecutarse en una amplia gama de hardware.

Los metacomandos forman parte de la API de Direct3D 12, aunque están acoplados de forma flexible. Un metacomando se identifica mediante un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)fijo, mientras que casi todo lo demás (desde su comportamiento y semántica hasta su firma y nombre) no forman parte estrictamente de la API de Direct3D 12. En su lugar, se especifica un metacomando entre su autor y el controlador que lo implementa. En este caso, el autor es DirectML. Los metacomandos son primitivos de Direct3D 12 (al igual que en el caso de las distribuciones y los envíos), para que se puedan grabar en una lista de comandos y estén programados para su ejecución.

DirectML acelera las cargas de trabajo de aprendizaje automático con un conjunto completo de metacomandos de machine learning. Por lo tanto, no es necesario escribir rutas de acceso de código específicas del proveedor para lograr la aceleración de hardware para la inferencia. Si tiene que ejecutarse en un chip de inteligencia artificial, DirectML usa ese hardware para acelerar considerablemente las operaciones como la circunvolución. Puede tomar el mismo código que ha escrito, sin modificarlo, ejecutarlo en un chip que no sea de inteligencia artificial (quizás la GPU integrada en el portátil) y seguir teniendo una excelente aceleración de hardware de GPU. Y si no hay ninguna GPU disponible, DirectML recurre a la CPU.
