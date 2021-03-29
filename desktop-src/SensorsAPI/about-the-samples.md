---
description: El Windows SDK incluye ejemplos de código y herramientas útiles para ayudarle a entender y usar el sensor de Windows y la plataforma de ubicación y las API relacionadas.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Acerca de los ejemplos y las herramientas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912237"
---
# <a name="about-the-samples-and-tools"></a>Acerca de los ejemplos y las herramientas

El Windows SDK incluye ejemplos de código y herramientas útiles para ayudarle a entender y usar el sensor de Windows y la plataforma de ubicación y las API relacionadas.

## <a name="samples"></a>Ejemplos

El Windows SDK incluye los siguientes ejemplos de API de sensor. Puede encontrar los ejemplos de API de sensor en la carpeta denominada \\ Samples \\ WinUI \\ Sensors, donde ha instalado el Windows SDK. Por ejemplo, si instaló el Windows SDK en la unidad C, encontraría los ejemplos en la siguiente carpeta: C: archivos de \\ programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ WinUI \\ Sensors.



| Nombre del ejemplo       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | En este ejemplo de MFC se muestra cómo usar la API de sensor mediante la lectura de datos de sensores de luz ambiente en el equipo y el cambio de tamaño de texto en función de las condiciones de iluminación. Puede ver el código que muestra cómo administrar eventos y cómo solicitar permisos de usuario. También puede ver un ejemplo de cómo administrar la interfaz de usuario en función de las condiciones de iluminación variables. Para obtener más información, consulte [creación de Light-Aware interfaces de usuario](creating-light-aware-user-interfaces.md).<br/> Debe tener instalado Visual Studio 2008 para compilar este ejemplo.<br/> |



 

Para obtener más información, vea el archivo denominado ReadMe.txt que se incluye con el ejemplo.

También puede descargar el ejemplo AmbientLightAware de la galería de código. Para obtener más información, consulte la página de descarga compatible con la [luz ambiente](/samples/browse/?redirectedfrom=MSDN-samples) .

## <a name="tools"></a>Herramientas

El Windows SDK incluye un sensor de luz virtual que puede usar para simular un dispositivo de sensor de luz basado en hardware. Puede usar esta herramienta para proporcionar datos al ejemplo AmbientLightAware para ver cómo funciona el código del ejemplo.

En la tabla siguiente se describen los archivos que se deben usar para ejecutar el sensor de luz virtual. Puede encontrar estos archivos en la carpeta denominada bin, donde ha instalado el Windows SDK. Por ejemplo, si instaló el Windows SDK en la unidad C en un equipo de 32 bits, encontraría los archivos del sensor de luz virtual en la carpeta siguiente: C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin. En equipos de 64 bits, debe usar la versión de 64 bits de la herramienta. En el Windows SDK, las herramientas de 64 bits se encuentran en la subcarpeta denominada x64.



| Nombre de archivo                    | Descripción                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Este programa proporciona un control deslizante que le permite cambiar el nivel de los datos claros que el sensor virtual informa. |
| VirtualLightSensorDriver.dll | Controlador de sensor lógico que simula un sensor ligero.                                                                       |
| VirtualLightSensorDriver. inf | El archivo INF para el controlador del sensor de luz virtual.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Instalación del sensor de luz virtual

Antes de usar la aplicación de sensor de luz virtual, debe instalar el controlador de sensor lógico. Siga estos pasos:

1.  Abra una ventana de comandos como administrador.
2.  Cambie a la carpeta Windows SDK bin.
3.  Escriba **pnputil-a VirtualLightSensorDriver. inf**.
4.  Cuando se le solicite, haga clic en **instalar este software de controlador de todos modos**.
5.  Espere a que la ventana de comandos informe de que el controlador se ha instalado correctamente.

### <a name="running-the-virtual-light-sensor"></a>Ejecutar el sensor de luz virtual

Para ejecutar el sensor de luz virtual, simplemente haga doble clic en el archivo. exe. Cuando se le solicite, asegúrese de habilitar el sensor.

Al ejecutar el programa, es posible que observe que hay un retraso antes de que el sensor esté disponible. La interfaz de usuario del sensor virtual de luz mostrará el mensaje "en espera" en la barra de título mientras el administrador del sensor lógico crea un nodo de dispositivo para el sensor lógico. Después de que el mensaje en espera salga, puede usar el control deslizante para establecer el nivel de salida de lux para el sensor de luz virtual.

En la imagen siguiente se muestra la interfaz de usuario del sensor de luz virtual en estado listo.

![interfaz de usuario del sensor virtual Light](images/virtuallightsensor.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los sensores lógicos](about-logical-sensors.md)
</dt> <dt>

[**\_luz de categoría de sensor \_**](sensor-category-light.md)
</dt> </dl>

 

