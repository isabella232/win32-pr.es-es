---
title: Direct Machine Learning (DirectML)
description: Direct Machine Learning (DirectML) es una API de bajo nivel para machine learning. Tiene una conocida interfaz de programación (nativo C++, nano COM) flujo de trabajo en el estilo de DirectX 12.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104758"
---
# <a name="direct-machine-learning-directml"></a>Direct Machine Learning (DirectML)

Direct Machine Learning (DirectML) es una API de bajo nivel para machine learning. Tiene una conocida interfaz de programación (nativo C++, nano COM) flujo de trabajo en el estilo de DirectX 12. Puede integrar las cargas de trabajo de inferencia del aprendizaje automático en su juego, motor, middleware, back-end u otra aplicación. DirectML admite todo el hardware compatible con DirectX 12.

DirectML se ha introducido en Windows 10, versión 1903 y en la versión correspondiente de la Windows SDK.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Introducción a DirectML](dml-intro.md) | Direct Machine Learning (DirectML) es una API de bajo nivel para machine learning (ML). |
| [Enlaces en DirectML](dml-binding.md) | En DirectML, el *enlace* hace referencia a los datos adjuntos de los recursos a la canalización para que la GPU los use durante la inicialización y la ejecución de los operadores de aprendizaje automático. Estos recursos pueden ser, por ejemplo, los de entrada y salida, así como los recursos temporales o persistentes que necesita el operador. |
| [Barreras de UAV y barreras de estado de recursos en DirectML](dml-barriers.md) | Describe las ventajas de la corrección de barreras y cómo puede trabajar con ellas en DirectML. |
| [Uso de los progresos para expresar el relleno y el diseño de memoria](dml-strides.md) | Los DirectML se describen mediante propiedades conocidas como los *tamaños* y los *progresos* de la tensores. |
| [Duración y sincronización de los recursos](dml-resource-lifetime.md) | Para evitar un comportamiento no definido, la aplicación DirectML debe administrar correctamente la duración de los objetos y la sincronización entre la CPU y la GPU. |
| [Usar la capa de depuración DirectML](dml-debug-layer.md) | La capa de depuración DirectML es un componente opcional en tiempo de desarrollo que le ayuda a depurar el código de DirectML. |
| [Control de errores y eliminación de dispositivos](dml-errors.md) | En este tema se describe cómo depurar la eliminación de dispositivos DirectML y otras condiciones de error. |
| [Funciones auxiliares de DirectML](dml-helper-functions.md) | Lista de códigos de funciones básicas de la aplicación auxiliar DirectML. |
| [Aplicaciones de ejemplo de DirectML](dml-min-app.md) | Vínculos a aplicaciones de ejemplo de DirectML, incluido un ejemplo de una aplicación DirectML mínima. |

## <a name="related-topics"></a>Temas relacionados

* [Guía de programación de Direct3D 12](directx-12-programming-guide.md)
