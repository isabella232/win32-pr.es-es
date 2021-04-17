---
description: Describe cómo Windows 10 usa conjuntos de API en las operaciones del cargador.
title: Operación de cargador del conjunto de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105721181"
---
# <a name="api-set-loader-operation"></a>Operación de cargador del conjunto de API

Los [conjuntos de API](windows-apisets.md) dependen de la compatibilidad del sistema operativo en el cargador de biblioteca para introducir de forma eficaz una redirección de espacio de nombres de módulo en el proceso de enlace de la biblioteca. El cargador de bibliotecas usa el [nombre del contrato de conjunto de API](windows-apisets.md#api-set-contract-names) para realizar una redirección en tiempo de ejecución de la referencia a un archivo binario de host de destino que hospeda la implementación adecuada del conjunto de API.

Cuando el cargador encuentra una dependencia en un conjunto de API en tiempo de ejecución, el cargador consulta los datos de configuración de la imagen para identificar el binario del host para un conjunto de API. Estos datos de configuración se denominan el **esquema de conjunto de API**. El esquema se ensambla como una propiedad del sistema operativo y la asignación entre los conjuntos de API y los archivos binarios puede diferir en función de los archivos binarios que se incluyen en un dispositivo determinado. El esquema permite que una función importada en un solo binario se enrute correctamente en distintos dispositivos, incluso si se ha cambiado el nombre de los módulos del host binario o se han refactorizado por completo en dispositivos Windows diferentes.

Windows 10 admite dos técnicas estándar para consumir e interactuar con conjuntos de API: **reenvío directo** y **reenvío inverso**.

### <a name="direct-forwarding"></a>Reenvío directo

En esta configuración, el código de consumo importa directamente un nombre de módulo de conjunto de API. Esta importación se resuelve en una sola operación y es el método más eficaz con la sobrecarga mínima. Conceptualmente, esta resolución puede apuntar a archivos binarios diferentes en dispositivos de Windows 10 diferentes, como se muestra en el ejemplo siguiente:

Conjunto de API importado: **api-feature1-l1-1-0.dll**
-  Windows PC: > **feature1.dll**
-  HoloLens: > **feature1_holo.dll**
-  **feature1_iot.dll** de IoT->

Dado que las asignaciones se mantienen en un repositorio de datos de esquema personalizado, significa que un nombre de conjunto de API que termina con **. dll** no hace referencia directamente a un archivo en disco. La parte **. dll** del nombre del conjunto de API solo es una Convención requerida por el cargador. El nombre del conjunto de API es más parecido a un alias o un nombre virtual para un archivo DLL físico. Esto hace que el nombre sea portátil en todo el intervalo de dispositivos Windows 10.

### <a name="reverse-forwarding"></a>Reenvío inverso

Aunque los nombres de los conjuntos de API proporcionan un espacio de nombres estable para los módulos en todos los dispositivos, no siempre es práctico convertir cada binario en este nuevo sistema. Por ejemplo, una aplicación puede haber estado en uso común durante muchos años y es posible que no sea factible volver a compilar los archivos binarios de la aplicación. Además, es posible que algunas aplicaciones deban seguir ejecutándose en sistemas compilados antes de que se introdujeran determinados conjuntos de API.

Para dar cabida a este nivel de compatibilidad, se proporciona un sistema de *reenviadores* en todos los dispositivos de Windows 10 que cubren un subconjunto de la superficie de la API de Win32. Estos reenviadores usan los nombres de módulo que se introdujeron en los equipos Windows y aprovechan el sistema de conjunto de API para proporcionar compatibilidad en todos los dispositivos Windows 10.

La operación del cargador se comporta de la siguiente manera:

1.  En un dispositivo que no sea un equipo con Windows, al cargador se le presenta una dependencia de nombre de módulo de PC de Windows heredada que no está presente en el dispositivo.
2.  El cargador localiza un reenviador de conjunto de API para este módulo y lo carga en la memoria.
3.  El reenviador tiene una asignación para el conjunto de API para la función especificada a la que se llama.
4.  El cargador busca el archivo binario de host adecuado para el dispositivo especificado.

Conceptualmente, la asignación tiene el siguiente aspecto:

DLL importada: **feature1.dll**
- Windows PC: > **feature1.dll**
- HoloLens-> **feature1.dll** reenviador-> **api-feature1-l1-1-0.dll**  ->  **feature1_holo.dll**
- IOT-> **feature1.dll** reenviador-> **api-feature1-l1-1-0.dll**  ->  **feature1_iot.dll**

El resultado final es funcionalmente igual que el [reenvío directo](#direct-forwarding), pero lo consigue de forma que se maximice la compatibilidad de aplicaciones.

> [!NOTE]
> El reenvío inverso proporciona cobertura solo para un subconjunto de la superficie de la API de Win32. No permite que las aplicaciones destinadas a versiones de escritorio de Windows 10 se ejecuten en todos los dispositivos Windows 10.
