---
description: El servicio de disco virtual (VDS) administra una amplia gama de configuraciones de almacenamiento, desde escritorios de un solo disco hasta matrices de almacenamiento externo. El servicio expone una interfaz de programación de aplicaciones (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Servicio de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677931"
---
# <a name="virtual-disk-service"></a>Servicio de disco virtual

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM de servicio de disco virtual se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

## <a name="purpose"></a>Propósito

El servicio de disco virtual (VDS) administra una amplia gama de configuraciones de almacenamiento, desde escritorios de un solo disco hasta matrices de almacenamiento externo. El servicio expone una interfaz de programación de aplicaciones (API).

## <a name="where-applicable"></a>Donde sea aplicable

A partir de Windows 8 y Windows Server 8, la interfaz COM de servicio de disco virtual se sustituye por la API de administración de almacenamiento, una interfaz de programación basada en WMI. Para administrar los subsistemas de almacenamiento, los discos, las particiones y los volúmenes de (Windows), se recomienda encarecidamente usar la API de administración de almacenamiento. Para obtener más información, consulte la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

En el caso de todos los usos excepto los volúmenes de arranque reflejado (mediante un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están desusados. En el caso de los datos que requieren resistencia frente a errores de unidad, use espacios de almacenamiento, una solución de virtualización de almacenamiento resistente. Para obtener más información, consulte la [vista previa técnica de espacios de almacenamiento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Los desarrolladores de aplicaciones que usan las interfaces descritas en esta guía pueden consultar y configurar un conjunto heterogéneo de almacenamiento administrado internamente y proporcionado por el proveedor. VDS oculta de las aplicaciones las complejidades asociadas con el almacenamiento, lo que permite que el servicio sea independiente del proveedor y de la tecnología.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está destinada a los desarrolladores de aplicaciones que están familiarizados con las capacidades de almacenamiento de las plataformas de Microsoft Windows y que conocen el desarrollo COM.

La guía también está destinada a los fabricantes de subsistemas de hardware que desarrollan y admiten programas de proveedor de hardware VDS.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

VDS es compatible con Windows Server 2003, Windows Vista y versiones posteriores. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, consulte la sección de requisitos de la documentación de ese elemento.

Se admite la ejecución de aplicaciones VDS de 32 bits en WOW64, pero los proveedores de VDS de 64 bits deben ejecutarse como aplicaciones nativas en versiones de Windows de 64 bits.

VDS está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows. Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el [centro de descarga de Windows](https://www.microsoft.com/download/details.aspx?id=8279). Esta versión del Windows SDK se puede usar para desarrollar aplicaciones de VDS para Windows Server 2003, Windows Vista y versiones posteriores. También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el centro de descarga de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                         | Descripción                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Acerca de VDS](about-vds.md)<br/>         | Describe el modelo de objetos VDS, las estrategias de configuración de almacenamiento y las notificaciones de VDS.<br/>    |
| [Uso de VDS](using-vds.md)<br/>         | Describe cómo usar VDS para consultar y configurar dispositivos de almacenamiento.<br/>                            |
| [Referencia de VDS](vds-reference.md)<br/> | Describe las constantes de VDS, los tipos de datos, las enumeraciones, las interfaces, las estructuras y los códigos de error.<br/> |



 

 

