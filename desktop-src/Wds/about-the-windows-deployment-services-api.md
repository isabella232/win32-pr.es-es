---
title: Acerca de la API Windows Deployment Services
description: Windows Deployment Services (WDS) es un conjunto de componentes que permiten la implementación de sistemas operativos de Windows, especialmente Windows Vista y versiones posteriores y Windows Server 2008 y versiones posteriores.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows Deployment Services Windows Deployment Services , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098685"
---
# <a name="about-the-windows-deployment-services-api"></a>Acerca de la API Windows Deployment Services

Windows Deployment Services (WDS) es un conjunto de componentes que permiten la implementación de sistemas operativos de Windows, especialmente Windows Vista y versiones posteriores y Windows Server 2008 y versiones posteriores. Puede usarlo para configurar nuevos equipos mediante instalaciones basadas en red.

Los OEM, los generadores de sistemas y los profesionales de TI corporativos que buscan información sobre cómo implementar Windows en equipos nuevos deben ver la información sobre la solución WDS estándar en la guía paso a paso de actualización de [Windows Deployment Services](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) y el Kit de instalación automatizada [(LOK) de Windows.](https://www.microsoft.com/download/details.aspx?id=10333)

En entornos en los que no se puede usar la solución WDS estándar, la API de WDS permite el acceso mediante programación a algunos componentes de WDS.

-   Las [Windows de servidor de Deployment Services](windows-deployment-services-server-functions.md) proporcionan acceso mediante programación al servidor de entorno de ejecución previo al arranque WDS (PXE). Los componentes del servidor WDS incluyen un servidor PXE y un servidor protocolo de transferencia de archivos trivial (TFTP) para el arranque de red de un equipo para cargar e instalar un sistema operativo.
-   Las [Windows cliente de Deployment Services](windows-deployment-services-client-functions.md) proporcionan acceso mediante programación al cliente WDS. Los componentes de cliente de WDS incluyen una interfaz gráfica de usuario que se ejecuta en el entorno de preins instalación de Windows (Windows PE) y se comunica con los componentes del servidor para seleccionar e instalar una imagen de sistema operativo.
-   No hay ninguna API para los componentes de administración de WDS. estos componentes son un conjunto de herramientas que puede usar para administrar el servidor, las imágenes del sistema operativo y las cuentas del equipo cliente. Para obtener más información sobre los componentes de administración de WDS, vea [The Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

El servidor PXE de WDS consta de un servidor PXE y un proveedor PXE. El servidor PXE contiene la funcionalidad de red principal. El servidor PXE admite interfaces de complemento que se conocen como proveedores PXE. Este modelo de proveedor permite el desarrollo de soluciones PXE personalizadas a la vez que sigue utilizando la base de código de red del servidor PXE principal.

-   Los desarrolladores pueden usar [Windows Deployment Services](windows-deployment-services-server-functions.md) Server Functions para escribir un archivo DLL para que un proveedor personalizado reemplace o ejecute junto con la capa de negociación de información de arranque (BINL) estándar en un servidor WDS. Por ejemplo, el proveedor personalizado puede usar un archivo de texto como su almacén de datos en lugar de Active Directory.
-   Los desarrolladores pueden usar [Windows Deployment Services](windows-deployment-services-server-functions.md) Server Functions para escribir un proveedor de filtros que se secuencia antes de BINL, o cualquier otro proveedor PXE, en la lista ordenada de proveedores registrados. A continuación, el segundo proveedor solo atiende las solicitudes PXE seleccionadas, mientras que el primer proveedor controla otras solicitudes. Por ejemplo, esto puede permitir que el segundo proveedor registrado de la lista ordenada ofrezca una nueva funcionalidad sin interrumpir la solución WDS existente implementada en el primer proveedor.

El cliente WDS incluye una interfaz gráfica de usuario que se ejecuta en el entorno de preins instalación de Windows (Windows PE) y se comunica con los componentes del servidor para seleccionar e instalar una imagen de sistema operativo. La biblioteca cliente de WDS admite el desarrollo de aplicaciones cliente personalizadas que pueden usar un servidor WDS.

-   Los desarrolladores pueden usar [Windows de cliente](windows-deployment-services-client-functions.md) de Deployment Services para escribir su propia aplicación cliente personalizada que reemplace al cliente WDS. Por ejemplo, la aplicación personalizada puede enumerar las imágenes almacenadas en un servidor WDS y enviar mensajes de progreso de instalación al registro de eventos del servidor PXE.

## <a name="windows-deployment-services-samples"></a>Windows Ejemplos de Servicios de implementación

Hay disponible un proveedor PXE personalizado de ejemplo, un proveedor de filtros y una aplicación cliente WDS en el Kit de desarrollo de software (SDK) de Microsoft Windows; consulte [Microsoft Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)

Puede descargar los siguientes ejemplos de WDS en línea en la galería [de código de escritorio.](https://github.com/microsoft/Windows-classic-samples)

<dl>

[Windows Ejemplo de proveedor de filtros de Deployment Services](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Ejemplo de enumeración de imágenes de Deployment Services](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows Ejemplo de consumidor de multidifusión de Deployment Services](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Ejemplo de proveedor de multidifusión de Deployment Services](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Ejemplo de proveedor de Servicios de implementación](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Ejemplo del administrador de transporte de Deployment Services](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de servidor de Servicios de implementación de Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Uso de la API de cliente de Servicios de implementación de Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 