---
description: Un dispositivo de Direct3D es el componente de representación de Direct3D. Encapsula y almacena el estado de representación. Además, un dispositivo Direct3D realiza operaciones de transformación e iluminación y rasteriza una imagen en una superficie.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Dispositivos Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888604"
---
# <a name="direct3d-devices-direct3d-9"></a>Dispositivos Direct3D (Direct3D 9)

Un dispositivo de Direct3D es el componente de representación de Direct3D. Encapsula y almacena el estado de representación. Además, un dispositivo Direct3D realiza operaciones de transformación e iluminación y rasteriza una imagen en una superficie.

-   [XPDM frente a WDDM](xpdm-vs-wddm.md)
-   [Tipos de dispositivos (Direct3D 9)](device-types.md)
-   [Creación de un dispositivo (Direct3D 9)](creating-a-device.md)
-   [Modo de ventana Full-Screen usuario (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Selección de un dispositivo (Direct3D 9)](selecting-a-device.md)
-   [Dispositivos perdidos (Direct3D 9)](lost-devices.md)
-   [Determinar la compatibilidad con hardware (Direct3D 9)](determining-hardware-support.md)
-   [Procesamiento de datos de vértices (Direct3D 9)](processing-vertex-data.md)
-   [Elementos primitivos](primitives.md)

Desde el punto de vista arquitectónico, los dispositivos Direct3D contienen un módulo de transformación, un módulo de iluminación y un módulo de rasterización, como se muestra en el diagrama siguiente.

![diagrama de la arquitectura de dispositivos direct3d](images/d3ddev.png)

Direct3D admite actualmente dos tipos principales de dispositivos Direct3D:

-   Un dispositivo con rasterización acelerada por hardware y sombreado con procesamiento de vértices de hardware y software
-   Un dispositivo de referencia

Puede pensar en estos dispositivos como dos controladores independientes. Los controladores de software y los dispositivos de referencia se representan mediante controladores de software y el dispositivo se representa mediante un controlador de hardware. La manera más común de aprovechar estos dispositivos es usar el dispositivo para enviar aplicaciones y el dispositivo de referencia para las pruebas de características. Estos son proporcionados por terceros para emular dispositivos concretos, por ejemplo, hardware de desarrollo que aún no se ha publicado.

El dispositivo Direct3D que crea una aplicación debe corresponder a las funcionalidades del hardware en el que se ejecuta la aplicación. Direct3D proporciona funcionalidades de representación, ya sea mediante el acceso al hardware 3D instalado en el equipo o mediante la emulación de las funcionalidades de hardware 3D en software. Por lo tanto, Direct3D proporciona dispositivos para el acceso de hardware y la emulación de software.

Los dispositivos acelerados por hardware dan un rendimiento mucho mejor que los dispositivos de software. El tipo de dispositivo está disponible en todos los adaptadores gráficos compatibles con Direct3D. En la mayoría de los casos, las aplicaciones tienen como destino equipos que tienen aceleración de hardware y se basan en la emulación de software para dar cabida a equipos de gama inferior.

A excepción del dispositivo de referencia, los dispositivos de software no siempre admiten las mismas características que un dispositivo de hardware. Las aplicaciones siempre deben consultar las funcionalidades del dispositivo para determinar qué características se admiten.

Dado que el comportamiento del software y los dispositivos de referencia proporcionados con Direct3D 9 es idéntico al del dispositivo , el código de aplicación que se ha escrito para trabajar con el dispositivo de destino funcionará con el software o los dispositivos de referencia sin modificaciones. Tenga en cuenta que, aunque el comportamiento del software o del dispositivo de referencia proporcionado es idéntico al del dispositivo , las funcionalidades del dispositivo varían y un dispositivo de software determinado puede implementar un conjunto mucho más pequeño de funcionalidades.

## <a name="behaviors"></a>Comportamientos

Direct3D permite especificar el comportamiento de un dispositivo, así como el tipo del dispositivo. El [**método IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) permite una combinación de una o varias marcas de comportamiento para controlar los comportamientos globales del dispositivo Direct3D. Estos comportamientos especifican qué es y qué no se mantiene en la parte en tiempo de ejecución de Direct3D, y los tipos de dispositivo especifican qué controlador usar. Aunque algunas combinaciones de comportamientos de dispositivo no son válidas, es posible usar todos los comportamientos de dispositivo con todos los tipos de dispositivo. Por ejemplo, es válido especificar D3DDEVTYPE SW en un dispositivo creado \_ con D3DCREATE \_ PUREDEVICE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
