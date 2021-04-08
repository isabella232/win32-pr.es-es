---
title: Acerca de la API de servicios de implementación de Windows
description: Servicios de implementación de Windows (WDS) es un conjunto de componentes que permiten la implementación de sistemas operativos Windows, especialmente Windows Vista y versiones posteriores, y Windows Server 2008 y versiones posteriores.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Servicios de implementación de Windows servicios de implementación de Windows, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac4a904765f58ccf995c5bbc0a9413f8eb4d13c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995316"
---
# <a name="about-the-windows-deployment-services-api"></a>Acerca de la API de servicios de implementación de Windows

Servicios de implementación de Windows (WDS) es un conjunto de componentes que permiten la implementación de sistemas operativos Windows, especialmente Windows Vista y versiones posteriores, y Windows Server 2008 y versiones posteriores. Puede usarlo para configurar equipos nuevos mediante instalaciones basadas en red.

OEM, ensambladores de equipos y profesionales de TI corporativos que buscan información sobre cómo implementar Windows en equipos nuevos, deben ver la información acerca de la solución de WDS estándar en la [Guía paso a paso de actualización de servicios de implementación de Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) y el kit de [instalación automatizada de Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

En entornos donde no se puede usar la solución de WDS estándar, la API de WDS permite el acceso mediante programación a algunos componentes de WDS.

-   Las [funciones de servidor de servicios de implementación de Windows](windows-deployment-services-server-functions.md) proporcionan acceso mediante programación al servidor WDS entorno de ejecución previo al arranque (PXE). Los componentes de servidor de WDS incluyen un servidor PXE y un servidor de protocolo de transferencia de archivos trivial (TFTP) para la red que arranca un equipo para cargar e instalar un sistema operativo.
-   Las [funciones de cliente de servicios de implementación de Windows](windows-deployment-services-client-functions.md) proporcionan acceso mediante programación al cliente de WDS. Los componentes de cliente de WDS incluyen una interfaz gráfica de usuario que se ejecuta dentro del entorno de preinstalación de Windows (Windows PE) y se comunica con los componentes de servidor para seleccionar e instalar una imagen de sistema operativo.
-   No hay ninguna API para los componentes de administración de WDS. estos componentes son un conjunto de herramientas que puede usar para administrar el servidor, las imágenes del sistema operativo y las cuentas del equipo cliente. Para obtener más información sobre los componentes de administración de WDS, vea [la guía paso a paso de actualización de servicios de implementación de Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

El servidor WDS PXE consta de un servidor PXE y un proveedor PXE. El servidor PXE contiene la funcionalidad de red principal. El servidor PXE admite interfaces de complementos que se conocen como proveedores PXE. Este modelo de proveedor permite el desarrollo de soluciones PXE personalizadas a la vez que se sigue usando el código base de red de servidor PXE principal.

-   Los desarrolladores pueden usar las [funciones de servidor de servicios de implementación de Windows](windows-deployment-services-server-functions.md) para escribir un archivo DLL para que un proveedor personalizado se reemplace o se ejecute junto con la capa de negociación de información de arranque estándar (BINL) en un servidor WDS. Por ejemplo, el proveedor personalizado puede utilizar un archivo de texto como almacén de datos en lugar de Active Directory.
-   Los desarrolladores pueden usar las [funciones de servidor de servicios de implementación de Windows](windows-deployment-services-server-functions.md) para escribir un proveedor de filtros que se secuencia antes que BINL, o cualquier otro proveedor PXE, en la lista ordenada de proveedores registrados. El segundo proveedor solo atiende las solicitudes PXE seleccionadas, mientras que el primer proveedor controla otras solicitudes. Por ejemplo, esto puede permitir que el segundo proveedor registrado de la lista ordenada ofrezca nueva funcionalidad sin interrumpir la solución de WDS existente implementada en el primer proveedor.

El cliente WDS incluye una interfaz gráfica de usuario que se ejecuta dentro del entorno de preinstalación de Windows (Windows PE) y se comunica con los componentes de servidor para seleccionar e instalar una imagen de sistema operativo. La biblioteca de cliente de WDS admite el desarrollo de aplicaciones cliente personalizadas que pueden usar un servidor WDS.

-   Los desarrolladores pueden usar las [funciones de cliente de servicios de implementación de Windows](windows-deployment-services-client-functions.md) para escribir su propia aplicación cliente personalizada que reemplaza al cliente de WDS. Por ejemplo, la aplicación personalizada puede enumerar las imágenes almacenadas en un servidor WDS y enviar mensajes de progreso de la instalación al registro de eventos del servidor PXE.

## <a name="windows-deployment-services-samples"></a>Ejemplos de servicios de implementación de Windows

En el kit de desarrollo de software (SDK) de Microsoft Windows [, encontrará un](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)proveedor PXE personalizado de ejemplo, un proveedor de filtros y una aplicación cliente de WDS.

Puede descargar los siguientes ejemplos de WDS en línea en la [Galería de código de escritorio](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Ejemplo de proveedor de filtro de servicios de implementación de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Ejemplo de enumeración de imágenes de servicios de implementación de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Ejemplo de consumidor de multidifusión de servicios de implementación de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Ejemplo de proveedor de multidifusión de servicios de implementación de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Ejemplo de proveedor de servicios de implementación de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Ejemplo de administrador de transporte de servicios de implementación de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de servidor de Servicios de implementación de Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Uso de la API de cliente de Servicios de implementación de Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 