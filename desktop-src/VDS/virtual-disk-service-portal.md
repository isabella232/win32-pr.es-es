---
description: Virtual Disk Service (VDS) administra una amplia gama de configuraciones de almacenamiento, desde escritorios de un solo disco hasta matrices de almacenamiento externas. El servicio expone una interfaz de programación de aplicaciones (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Servicio de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c84217b1ca63debe3e117e33b2358e4b0e55697c02ce8e00ce7f764c1fbf692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137138"
---
# <a name="virtual-disk-service"></a>Servicio de disco virtual

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

## <a name="purpose"></a>Propósito

Virtual Disk Service (VDS) administra una amplia gama de configuraciones de almacenamiento, desde escritorios de un solo disco hasta matrices de almacenamiento externas. El servicio expone una interfaz de programación de aplicaciones (API).

## <a name="where-applicable"></a>Donde sea aplicable

A partir Windows 8 y Windows Server 8, la interfaz COM del servicio virtual de disco se sustituye por el Storage API de Administración, una interfaz de programación basada en WMI. Para administrar subsistemas de almacenamiento, (Windows) discos, particiones y volúmenes, se recomienda encarecidamente usar el Storage API de Administración. Para obtener más información, vea el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Para todos los usos excepto los volúmenes de arranque reflejados (con un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están en desuso. Para los datos que requieren resistencia frente a errores de unidad, use Espacios de almacenamiento, una solución de virtualización de almacenamiento resistente. Para obtener más información, [vea Espacios de almacenamiento Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Los desarrolladores de aplicaciones que usan las interfaces descritas en esta guía pueden consultar y configurar un conjunto heterogéneo de almacenamiento administrado internamente y proporcionado por el proveedor. VDS oculta a las aplicaciones las complejidades asociadas al almacenamiento, lo que hace que el servicio tanto el proveedor como la tecnología no se usen.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está pensada para desarrolladores de aplicaciones que están familiarizados con las funcionalidades de almacenamiento de las plataformas Windows Microsoft y que tienen conocimientos sobre el desarrollo COM.

La guía también está pensada para los fabricantes de subsistemas de hardware que desarrollan y admiten programas de proveedor de hardware VDS.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

VDS se admite en Windows Server 2003, Windows Vista y versiones posteriores. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la documentación de ese elemento.

Se admite la ejecución de aplicaciones VDS de 32 bits en WOW64, pero los proveedores VDS de 64 bits deben ejecutarse como aplicaciones nativas en versiones de Windows de 64 bits.

VDS está disponible en microsoft Windows Software Development Kit (SDK). Puede instalar el SDK para Windows 7 y Windows Server 2008 R2 desde el Centro [Windows descarga de archivos](https://www.microsoft.com/download/details.aspx?id=8279). Esta versión del SDK Windows se puede usar para desarrollar aplicaciones VDS para Windows Server 2003, Windows Vista y versiones posteriores. También puede descargar la [versión ISO](https://www.microsoft.com/download/details.aspx?id=8442) del SDK desde el Centro de Windows descarga.

## <a name="in-this-section"></a>En esta sección



| Tema                                         | Descripción                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Acerca de VDS](about-vds.md)<br/>         | Describe el modelo de objetos VDS, las estrategias de configuración de almacenamiento y las notificaciones VDS.<br/>    |
| [Uso de VDS](using-vds.md)<br/>         | Describe cómo usar VDS para consultar y configurar dispositivos de almacenamiento.<br/>                            |
| [Referencia de VDS](vds-reference.md)<br/> | Describe constantes VDS, tipos de datos, enumeraciones, interfaces, estructuras y códigos de error.<br/> |



 

 

