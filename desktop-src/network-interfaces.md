---
description: En este tema se describen los conceptos de interfaz de red de alto nivel en Windows, incluidas las formas en que se pueden identificar en el código y sus propiedades.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfaces de red
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: cc31be6062469750049a676807c2f8da24f473f1
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105700445"
---
# <a name="network-interfaces"></a>Interfaces de red

En este tema se describen los conceptos de interfaz de red de alto nivel en Windows, incluidas las formas en que se pueden identificar en el código y sus propiedades. 

> [!IMPORTANT]
> Este tema está dirigido a un público de desarrolladores, tanto para aplicaciones de red de escritorio de Windows como para controladores de red en modo kernel. No obstante, parte de la información que se presenta aquí también puede ser útil para los administradores del sistema que administran interfaces de red mediante cmdlets de PowerShell.

## <a name="overview"></a>Información general

Una *interfaz de red* es el punto en el que se conectan dos partes de equipos de red o capas de protocolo. Normalmente, se representa mediante una tarjeta de interfaz de red (NIC) física para la conexión entre un equipo y una red privada o pública. Sin embargo, también puede adoptar la forma de un componente de solo software, como la interfaz de bucle invertido ( `127.0.0.1` para IPv4 o `::1` para IPv6).

Las interfaces de red están definidas por el equipo de ingeniería de Internet (IETF) en [RFC 2863](https://tools.ietf.org/html/rfc2863) y no están diseñadas para ser definidas por Windows. Para obtener preguntas detalladas sobre el significado de los identificadores de interfaz de red, como el tipo de **carga, vea** las definiciones de los IETF. En el resto de este tema se describen los detalles de implementación específicos de Windows.

## <a name="network-interface-identifiers-and-properties"></a>Identificadores y propiedades de la interfaz de red

En Windows, una interfaz de red se puede identificar de maneras diferentes. Algunos de estos identificadores se usan para distinguir entre sí las interfaces de red, pero no todos los identificadores son igualmente adecuados para esa tarea debido a sus propiedades diferentes. Por lo general, las interfaces de red se identifican mediante una dirección de red para componentes externos. Por ejemplo, puede ser un identificador de nodo y un número de puerto, o simplemente un identificador de nodo único. 

En el código, una interfaz de red se puede identificar de muchas maneras. En la tabla siguiente se detallan las formas en que se puede identificar una interfaz de red junto con las propiedades asociadas. Se recomienda usar el GUID de interfaz (**ifGuid**) para programar a menos que una API específica requiera un identificador de interfaz de red diferente.

> [!NOTE]
> En la tabla siguiente, las celdas en **negrita** representan una propiedad que es deseable para los programadores de red.

| Identificador | Tamaño | Es único en el sistema | Es único en el mundo. | Es predecible | Se reciclará si se quita la NIC | Persiste entre reinicios | Los usuarios finales pueden modificar en cualquier momento | Los controladores pueden modificar en cualquier momento | Conocimientos generales de los usuarios finales | Siempre está presente |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 bytes** | **Sí** | No | No | Sí | No<sup>1</sup> | **No** | **No** | **Algunos**<sup>2</sup> | **Sí** |
| **NetLuid** | **8 bytes** | **Sí** | No | No | Sí | **Sí** | **No** | **No** | No | **Sí** |
| **ifGuid** | **16 bytes** | **Sí** | **Normalmente**<sup>3</sup> | No | **No** | **Sí** | **No** | **No** | No | **Sí** |
| **ifAlias** | 514 bytes | **Sí para NIC**<sup>4</sup> | No | A veces<sup>5</sup> | Sí | **Sí** | Sí | **No** | **Sí** | **Normalmente**<sup>4</sup> |
| **ifDescr** | 514 bytes | Normalmente<sup>6</sup> | No | No | Sí | **Sí** | **No** | Sí | **Sí** | **Ser** |
| **ifPhysAddress (dirección MAC)**| de 0 a 32 bytes | Normalmente, para NIC | **Normalmente, para NIC** | **Sí** | **Relacionado con el hardware** | **Sí** | **No** | **No** | **Sí** | **Normalmente** <sup>7</sup> |
| **IDENTIFICADOR de instancia de PnP** | Hasta 400 bytes | **Sí** | No | No | Sí | **Sí** | **No** | **No** | No | **Normalmente, para NIC**<sup>8</sup> |
| **Ubicación de PnP (número de ranura PCI)** | Hasta 400 bytes | **Sí** | No | **Sí** | Sí | **Sí** | **No** | **No** | Suele | A veces<sup>8, 9</sup> |

Notas para la tabla anterior:

1. No se garantiza que los **IfIndexes** sean estables a lo largo de los reinicios, aunque a menudo reciben el mismo valor que el arranque anterior. Por lo tanto, no se recomienda que los **Controladores utilicen el** modo de los
2. Algunos `netsh` comandos toman `ifIndex` o `index` como entrada. Por lo tanto, algunos usuarios administrativos están familiarizados con **la propiedad de modo de usuario** si usan el `netsh` comando con frecuencia.
3. Si un equipo se clona o se imagen, algunos de los GUID podrían ser los mismos. Además, algunas interfaces de red especiales, como la interfaz Teredo integrada, pueden tener el mismo GUID en todas las máquinas.
4. NetCfg exige que un **ifAlias** sea una cadena no vacía y que sea único entre todas las NIC. Sin embargo, el proveedor de la interfaz NDIS no lo hace. Thererfore, es posible encontrar interfaces de red especiales con nombres duplicados o vacíos. Esto se suele observar con los equipos de LBFO.
5. Solo si el firmware admite nombres de dispositivos coherentes. Typcically, los servidores tienen esta característica.
6. NetCfg asigna **ifDescrs** únicos a todas las interfaces de red. Sin embargo, los controladores pueden llamar a una API para cambiar el valor de **ifDescr** a cualquier cosa, incluido algo que no sea único. Algunos paquetes de software de terceros lo hacen.
7. No todos los tipos de medios tienen una "dirección MAC". Por ejemplo, algunos túneles no tienen este concepto y simplemente anuncian una matriz de bytes de longitud cero como su dirección de red.
8. Solo está presente en las interfaces de red que están respaldadas por un dispositivo PnP. Por ejemplo, las interfaces de bucle invertido, las interfaces de filtro ligeras, las interfaces proporcionadas por un proveedor de interfaz NDIS y algunas NIC especiales integradas no tienen dispositivos PnP que las respaldan.
9. Solo algunos buses de PnP admiten un identificador de ubicación de PnP. Los buses PCI y USB integrados sí lo hacen, mientras que los dispositivos enumerados por raíz no.

## <a name="visibility-to-developers"></a>Visibilidad para los desarrolladores

En la tabla anterior, todas las propiedades excepto las propiedades de Plug and Play (PnP) son visibles para las aplicaciones de escritorio en modo de usuario y los controladores de modo kernel a través de un encabezado compartido (Netioapi. h). Las propiedades de PnP son visibles a través del encabezado Devpkey. h y las usan las aplicaciones de escritorio en modo de usuario y los controladores de modo kernel. Por ejemplo, consulte la documentación de [DEVPKEY](/windows-hardware/drivers/install/devpkey-device-instanceid) .

La API de la [aplicación auxiliar de IP](/windows/desktop/IpHlp/ip-helper-start-page) también está disponible para las aplicaciones de escritorio en modo usuario y para los controladores de modo kernel.

La superficie de la API de UWP solo expone directamente la propiedad [ifGuid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) . Sin embargo, es posible que los desarrolladores de aplicaciones para UWP importen la función [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) mediante P/Invoke si son necesarias para tener acceso a otras propiedades de la interfaz de red.

## <a name="related-topics"></a>Temas relacionados

Para obtener las definiciones de base de información de administración (MIB) de las interfaces de red, consulte [RFC 2863](https://tools.ietf.org/html/rfc2863).

Para las interfaces de red NDIS en los controladores de red, consulte [interfaces de red NDIS](/windows-hardware/drivers/network/ndis-network-interfaces2).

Para consultar la referencia de la API de Netioapi. h, consulte el [encabezado Netioapi. h](/windows/desktop/api/netioapi/).
