---
description: Un dispositivo de Direct3D es el componente de representación de Direct3D. Encapsula y almacena el estado de representación. Además, un dispositivo Direct3D realiza transformaciones y operaciones de iluminación y rasteriza una imagen en una superficie.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Dispositivos Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274701"
---
# <a name="direct3d-devices-direct3d-9"></a>Dispositivos Direct3D (Direct3D 9)

Un dispositivo de Direct3D es el componente de representación de Direct3D. Encapsula y almacena el estado de representación. Además, un dispositivo Direct3D realiza transformaciones y operaciones de iluminación y rasteriza una imagen en una superficie.

-   [XPDM frente a WDDM](xpdm-vs-wddm.md)
-   [Tipos de dispositivos (Direct3D 9)](device-types.md)
-   [Crear un dispositivo (Direct3D 9)](creating-a-device.md)
-   [Modo de ventana de vs Full-Screen (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Seleccionar un dispositivo (Direct3D 9)](selecting-a-device.md)
-   [Dispositivos perdidos (Direct3D 9)](lost-devices.md)
-   [Determinar la compatibilidad de hardware (Direct3D 9)](determining-hardware-support.md)
-   [Procesar datos de vértices (Direct3D 9)](processing-vertex-data.md)
-   [Elementos primitivos](primitives.md)

En la arquitectura, los dispositivos de Direct3D contienen un módulo de transformación, un módulo de iluminación y un módulo de rasterización, como se muestra en el diagrama siguiente.

![diagrama de la arquitectura del dispositivo Direct3D](images/d3ddev.png)

Direct3D admite actualmente dos tipos principales de dispositivos de Direct3D:

-   Un dispositivo Hal con rasterización y sombreado acelerados por hardware con procesamiento de vértices de hardware y software
-   Un dispositivo de referencia

Estos dispositivos se pueden considerar como dos controladores independientes. Los dispositivos de software y de referencia están representados por controladores de software y el dispositivo Hal se representa mediante un controlador de hardware. La forma más común de aprovechar estos dispositivos es usar el dispositivo HAL para el envío de aplicaciones y el dispositivo de referencia para las pruebas de características. Son proporcionadas por terceros para emular dispositivos concretos, por ejemplo, hardware de desarrollo que todavía no se ha publicado.

El dispositivo Direct3D que crea una aplicación debe corresponderse con las capacidades del hardware en el que se ejecuta la aplicación. Direct3D proporciona funciones de representación, ya sea mediante el acceso al hardware 3D instalado en el equipo o mediante la emulación de las capacidades de hardware 3D en el software. Por lo tanto, Direct3D proporciona dispositivos para el acceso al hardware y la emulación de software.

Los dispositivos con aceleración de hardware proporcionan un rendimiento mucho mejor que los dispositivos de software. El tipo de dispositivo Hal está disponible en todos los adaptadores de gráficos compatibles con Direct3D. En la mayoría de los casos, las aplicaciones tienen como destino los equipos que tienen aceleración de hardware y se basan en la emulación de software para dar cabida a equipos de nivel inferior.

A excepción del dispositivo de referencia, los dispositivos de software no siempre admiten las mismas características que un dispositivo de hardware. Las aplicaciones siempre deben consultar las funcionalidades del dispositivo para determinar qué características se admiten.

Dado que el comportamiento del software y los dispositivos de referencia proporcionados con Direct3D 9 es idéntico al del dispositivo HAL, el código de aplicación creado para trabajar con el dispositivo Hal funcionará con el software o los dispositivos de referencia sin modificaciones. Tenga en cuenta que, aunque el software proporcionado o el comportamiento del dispositivo de referencia es idéntico al del dispositivo HAL, las capacidades del dispositivo varían y un dispositivo de software concreto puede implementar un conjunto de funcionalidades mucho menor.

## <a name="behaviors"></a>Comportamientos

Direct3D le permite especificar el comportamiento de un dispositivo, así como el tipo de dispositivo. El método [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) permite una combinación de una o varias de las marcas de comportamiento para controlar los comportamientos globales del dispositivo Direct3D. Estos comportamientos especifican qué es y no se mantiene en la parte de tiempo de ejecución de Direct3D y los tipos de dispositivos especifican qué controlador usar. Aunque algunas combinaciones de los comportamientos de los dispositivos no son válidas, es posible usar todos los comportamientos de los dispositivos con todos los tipos de dispositivos. Por ejemplo, es válido especificar D3DDEVTYPE \_ SW en un dispositivo creado con D3DCREATE \_ PUREDEVICE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
