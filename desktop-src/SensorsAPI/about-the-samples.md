---
description: El SDK Windows incluye herramientas y ejemplos de código útiles para ayudarle a comprender y usar la plataforma de sensor y ubicación de Windows y las API relacionadas.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Acerca de las herramientas y ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eecd388323ae8a548fcfefbc116224125b4b137f85231c56ea66235b3233fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890329"
---
# <a name="about-the-samples-and-tools"></a>Acerca de las herramientas y ejemplos

El SDK Windows incluye herramientas y ejemplos de código útiles para ayudarle a comprender y usar la plataforma de sensor y ubicación de Windows y las API relacionadas.

## <a name="samples"></a>Ejemplos

El SDK Windows incluye los siguientes ejemplos de Sensor API. Puede encontrar los ejemplos de Sensor API en la carpeta \\ denominada Samples winui Sensors (Ejemplos de sensores winui), donde instaló el \\ \\ SDK Windows. Por ejemplo, si ha instalado el SDK de Windows en la unidad C, encontrará los ejemplos en la carpeta siguiente: C: Archivos de programa SDK de \\ \\ Microsoft Windows \\ \\ v7.0 \\ Ejemplos de \\ sensores \\ winui.



| Nombre del ejemplo       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | En este ejemplo de MFC se muestra cómo usar Sensor API mediante la lectura de datos de sensores de luz ambiental en el equipo y el cambio del tamaño del texto según las condiciones de iluminación. Puede ver código que muestra cómo administrar eventos y cómo solicitar permisos de usuario. También puede ver un ejemplo de cómo administrar la interfaz de usuario en función de las distintas condiciones de iluminación. Para obtener más información, vea [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).<br/> Debe tener instalado Visual Studio 2008 para compilar este ejemplo.<br/> |



 

Para obtener más información, vea el archivo denominado ReadMe.txt que se incluye con el ejemplo.

También puede descargar el ejemplo AmbientLightAware de la Galería de código. Para obtener más información, consulte la [página de descarga de Ambient Light Aware.](/samples/browse/?redirectedfrom=MSDN-samples)

## <a name="tools"></a>Herramientas

El SDK Windows incluye un sensor de luz virtual que puede usar para simular un dispositivo de sensor de luz basado en hardware. Puede usar esta herramienta para proporcionar datos al ejemplo AmbientLightAware para ver cómo funciona el código del ejemplo.

En la tabla siguiente se describen los archivos que debe usar para ejecutar el sensor de luz virtual. Puede encontrar estos archivos en la carpeta denominada Bin, donde instaló el SDK Windows. Por ejemplo, si instaló el SDK de Windows en la unidad C en un equipo de 32 bits, encontraría los archivos de sensor de luz virtual en la carpeta siguiente: C: Archivos de programa SDK de \\ \\ Microsoft Windows bin \\ \\ v7.0. \\ En equipos de 64 bits, debe usar la versión de 64 bits de la herramienta. En el SDK Windows, las herramientas de 64 bits se encuentran en la subcarpeta denominada x64.



| Nombre de archivo                    | Descripción                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Este programa proporciona un control deslizante que permite cambiar el nivel de los datos claros que el sensor virtual notifica. |
| VirtualLightSensorDriver.dll | Controlador de sensor lógico que simula un sensor de luz.                                                                       |
| VirtualLightSensorDriver.inf | Archivo INF para el controlador del sensor de luz virtual.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Instalación del sensor de luz virtual

Antes de usar la aplicación de sensor de luz virtual, debe instalar el controlador del sensor lógico. Siga estos pasos:

1.  Abra una ventana de comandos como administrador.
2.  Cambie a la carpeta bin Windows SDK.
3.  Escriba **pnputil -a VirtualLightSensorDriver.inf**.
4.  Cuando se le solicite, haga **clic en Instalar este software de controlador de todos modos.**
5.  Espere a que la ventana de comandos informe de que el controlador se instaló correctamente.

### <a name="running-the-virtual-light-sensor"></a>Ejecución del sensor de luz virtual

Para ejecutar el sensor de luz virtual, simplemente haga doble clic en .exe archivo. Asegúrese de habilitar el sensor cuando se le solicite.

Al ejecutar el programa, es posible que observe que hay un retraso antes de que el sensor esté disponible. La interfaz de usuario del sensor de luz virtual mostrará el mensaje "Esperando" en la barra de título, mientras que el administrador de sensores lógicos crea un nodo de dispositivo para el sensor lógico. Una vez que el mensaje en espera desaparece, puede usar el control deslizante para establecer el nivel de salida del sensor de luz virtual.

En la imagen siguiente se muestra la interfaz de usuario del sensor de luz virtual en su estado listo.

![interfaz de usuario del sensor de luz virtual](images/virtuallightsensor.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los sensores lógicos](about-logical-sensors.md)
</dt> <dt>

[**SENSOR \_ CATEGORY \_ LIGHT**](sensor-category-light.md)
</dt> </dl>

 

