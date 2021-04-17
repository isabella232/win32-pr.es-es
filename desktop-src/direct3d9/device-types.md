---
description: Tipos de dispositivos (Direct3D 9)
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: Tipos de dispositivos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359924"
---
# <a name="device-types-direct3d-9"></a>Tipos de dispositivos (Direct3D 9)

## <a name="hal-device"></a>Dispositivo HAL

El tipo de dispositivo principal es el dispositivo HAL, que admite la rasterización acelerada de hardware y el procesamiento de vértices de hardware y software. Si el equipo en el que se ejecuta la aplicación está equipado con un adaptador de pantalla que admite Direct3D, la aplicación debe usarlo para las operaciones de Direct3D. Los dispositivos HAL de Direct3D implementan todo o parte de los módulos de transformación, iluminación y rasterización en el hardware.

Las aplicaciones no tienen acceso directo a los adaptadores de gráficos. Llaman a funciones y métodos de Direct3D. Direct3D accede al hardware a través de la HAL. Si el equipo en el que se ejecuta la aplicación admite la HAL, obtendrá el mejor rendimiento mediante el uso de un dispositivo Hal.

Para crear un dispositivo HAL, llame a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) con D3DDEVTYPE \_ Hal como el tipo de dispositivo.

## <a name="reference-device"></a>Dispositivo de referencia

Direct3D admite un tipo de dispositivo adicional denominado rasterizador de referencia o dispositivo de referencia. A diferencia de un dispositivo de software, el rasterizador de referencia es compatible con todas las características de Direct3D. Este dispositivo está diseñado para usarse con fines de depuración y, por tanto, solo está disponible en los equipos en los que se ha instalado el SDK de DirectX. Dado que estas características se implementan para obtener una precisión en lugar de la velocidad y se implementan en el software, los resultados no son muy rápidos. El rasterizador de referencia hace uso de instrucciones de CPU especiales siempre que sea posible, pero no está diseñado para aplicaciones comerciales. Use el rasterizador de referencia solo para fines de prueba o demostración. Para crear un dispositivo de referencia, llame al método [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) con \_ la referencia D3DDEVTYPE como el tipo de dispositivo.

## <a name="hal-vs-ref-devices"></a>HAL frente a dispositivos REF

Los dispositivos HAL (capa de abstracción de hardware) y los dispositivos REF (rasterizador de referencia) son los dos tipos principales de dispositivo Direct3D; la primera se basa en la compatibilidad de hardware y es muy rápida, pero es posible que no sea compatible con todo. mientras que el segundo no utiliza aceleración de hardware, por lo que es muy lento, pero se garantiza que admita todo el conjunto de características de Direct3D de la manera correcta. En general, solo tendrá que usar dispositivos HAL, pero si usa alguna característica avanzada que la tarjeta gráfica no admita, es posible que tenga que revertir a la referencia.

La otra vez que desee usar REF es si el dispositivo HAL está produciendo resultados extraños; es decir, está seguro de que el código es correcto, pero el resultado no es lo que espera. Se garantiza que el dispositivo de referencia se comporta correctamente, por lo que es posible que desee probar la aplicación en el dispositivo de referencia y ver si el comportamiento extraño continúa. Si no es así, significa que (a) la aplicación supone que la tarjeta gráfica es compatible con algo que no sea o (b) es un error de controlador. Si todavía no funciona con el dispositivo de referencia, se trata de un error de aplicación.

## <a name="hardware-vs-software-vertex-processing"></a>Procesamiento de vértices de software y hardware

El hardware frente al procesamiento de vértices de software solo se aplica realmente a los dispositivos HAL. Al hacer que los vértices se inserten a través de la canalización, es necesario que se transformen (por las matrices del mundo, de la vista y de la proyección) y que se iluminen (mediante las luces integradas de D3D's). esta fase de procesamiento se conoce como T&L (para la transformación & iluminación). El procesamiento de vértices de hardware significa que esto se hace en hardware, si el hardware lo admite; Ergo, el procesamiento de vértices de software es el software. La práctica general es intentar crear un dispositivo T&L de hardware primero y, si se produce un error, probar de forma mixta y, si se produce un error, probar el software. (Si se produce un error en el software, determine y salga con un error).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
