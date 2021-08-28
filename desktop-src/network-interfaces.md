---
description: En este tema se describen los conceptos de interfaz de red de alto nivel Windows, incluidas las formas en que se pueden identificar en el código y sus propiedades.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfaces de red
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: d74c875b579a34464190ca039e0176b8c01bef671b0ea6c24581023a49988645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825465"
---
# <a name="network-interfaces"></a>Interfaces de red

En este tema se describen los conceptos de interfaz de red de alto nivel Windows, incluidas las formas en que se pueden identificar en el código y sus propiedades. 

> [!IMPORTANT]
> Este tema está destinado a un público desarrollador, tanto para aplicaciones de Windows escritorio como para controladores de red en modo kernel. No obstante, parte de la información que se presenta aquí también puede ser útil para los administradores del sistema que administran interfaces de red a través de cmdlets de PowerShell.

## <a name="overview"></a>Información general

Una *interfaz de red* es el punto donde se conectan dos partes de equipos de red o capas de protocolo. Normalmente, esto se representa mediante una tarjeta de interfaz de red (NIC) física para la conexión entre un equipo y una red privada o pública. Sin embargo, también puede tomar la forma de un componente de solo software, como la interfaz de bucleback ( para `127.0.0.1` IPv4 `::1` o para IPv6).

El Grupo de tareas de ingeniería de Internet (IETF) define las interfaces de red en [RFC 2863](https://tools.ietf.org/html/rfc2863) y no están pensadas para definirse por Windows. Para obtener preguntas detalladas sobre el significado de los identificadores de interfaz de red como **ifIndex**, vea las definiciones de IETF de ellos. En el resto de este tema se de Windows detalles de implementación específicos.

## <a name="network-interface-identifiers-and-properties"></a>Identificadores y propiedades de la interfaz de red

En Windows, una interfaz de red se puede identificar de maneras diferentes. Algunos de estos identificadores se usan para distinguir las interfaces de red entre sí, pero no todos los identificadores son igualmente adecuados para esa tarea debido a sus distintas propiedades. Por lo general, las interfaces de red se identifican mediante una dirección de red a componentes externos. Por ejemplo, puede ser un identificador de nodo y un número de puerto, o simplemente un identificador de nodo único. 

En el código, una interfaz de red se puede identificar de muchas maneras. En la tabla siguiente se detallan las formas en que se puede identificar una interfaz de red junto con las propiedades asociadas. Se recomienda usar el GUID de interfaz (**ifGuid**) para la programación, a menos que una API específica requiera un identificador de interfaz de red diferente.

> [!NOTE]
> En la tabla siguiente, las **celdas en** negrita representan una propiedad que es deseable para los programadores de redes.

| Identificador | Size | Es único en el sistema | Es único en el mundo | Es predecible | Se reciclará si se quita la NIC | Se conserva entre reinicios | Los usuarios finales pueden modificar en cualquier momento | Los controladores se pueden modificar en cualquier momento | Familiaridad general con los usuarios finales | Siempre está presente |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 bytes** | **Sí** | No | No | Sí | No<sup>1</sup> | **No** | **No** | **Unos**<sup>2</sup> | **Sí** |
| **NetLuid** | **8 bytes** | **Sí** | No | No | Sí | **Sí** | **No** | **No** | No | **Sí** |
| **ifGuid** | **16 bytes** | **Sí** | **Normalmente**<sup>3</sup> | No | **No** | **Sí** | **No** | **No** | No | **Sí** |
| **ifAlias** | 514 bytes | **Sí para NIC**<sup>4</sup> | No | A<sup>veces 5</sup> | Sí | **Sí** | Sí | **No** | **Sí** | **Normalmente,**<sup>4</sup> |
| **ifDescr** | 514 bytes | Normalmente,<sup>6</sup> | No | No | Sí | **Sí** | **No** | Sí | **Sí** | **Generalmente** |
| **ifPhysAddress (DIRECCIÓN MAC)**| De 0 a 32 bytes | Normalmente, para NIC | **Normalmente, para NIC** | **Sí** | **Vinculado al hardware** | **Sí** | **No** | **No** | **Sí** | **Normalmente** <sup>7</sup> |
| **Id. de instancia de PnP** | Hasta 400 bytes | **Sí** | No | No | Sí | **Sí** | **No** | **No** | No | **Normalmente, para NIC**<sup>8</sup> |
| **Ubicación de PnP (número de ranura PCI)** | Hasta 400 bytes | **Sí** | No | **Sí** | Sí | **Sí** | **No** | **No** | Algunas veces | A<sup>veces 8,9</sup> |

Notas de la tabla anterior:

1. **No se garantiza que ifIndexes** sea estable en los reinicios, aunque a menudo reciben el mismo valor que el arranque anterior. Por lo tanto, no se recomienda que los controladores usen **ifIndex excepto** cuando lo requiera una API.
2. Algunos `netsh` comandos toman , o , como `ifIndex` `index` entrada. Por lo tanto, algunos usuarios administrativos están familiarizados con la **propiedad ifIndex** si usan el `netsh` comando con frecuencia.
3. Si una máquina se clona o se imaged, algunos de los GUID podrían ser los mismos. Además, ciertas interfaces de red especiales, como la interfaz integrada de Teredo, podrían tener el mismo GUID en todas las máquinas.
4. NetCfg exige que **ifAlias** sea una cadena no vacía y sea única entre todas las NIC. Sin embargo, el proveedor de interfaz NDIS no lo hace. Por lo tanto, es posible encontrar interfaces de red especiales con nombres duplicados o vacíos. Esto se ve normalmente con los equipos lbfo.
5. Solo si el firmware admite la nomenclatura coherente de dispositivos. De forma típica, los servidores tienen esta característica.
6. NetCfg asigna **ifDescrs único** a todas las interfaces de red. Sin embargo, los controladores pueden llamar a una API para cambiar **ifDescr** a cualquier cosa, incluido algo que no es único. Algunos paquetes de software de terceros hacen esto.
7. No todos los tipos de medios tienen una "dirección MAC". Por ejemplo, algunos túneles no tienen este concepto y simplemente anuncian una matriz de bytes de longitud cero como su dirección de red.
8. Solo está presente en las interfaces de red que están copiadas por un dispositivo PnP. Por ejemplo, las interfaces de bucle atrás, las interfaces de filtro ligeras, las interfaces proporcionadas por un proveedor de interfaces NDIS y ciertas NIC integradas especiales no tienen dispositivos PnP de respaldo.
9. Solo algunos buses PnP admiten un identificador de ubicación pnP. Los buses PCI y USB integrados sí, mientras que los dispositivos enumerados en la raíz no lo hacen.

## <a name="visibility-to-developers"></a>Visibilidad para desarrolladores

En la tabla anterior, todas las propiedades excepto las propiedades Plug and Play (PnP) son visibles para las aplicaciones de escritorio en modo de usuario y los controladores de modo kernel a través de un encabezado compartido (Netioapi.h). Las propiedades pnP son visibles a través del encabezado Devpkey.h y las usan tanto las aplicaciones de escritorio en modo de usuario como los controladores de modo kernel. Por ejemplo, consulte la documentación [de DEVPKEY.](/windows-hardware/drivers/install/devpkey-device-instanceid)

La [API del asistente](/windows/desktop/IpHlp/ip-helper-start-page) de IP también está disponible para las aplicaciones de escritorio en modo de usuario y los controladores de modo kernel.

La superficie de la API de UWP solo expone directamente [la propiedad ifGuid.](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) Sin embargo, es posible que los desarrolladores de aplicaciones para UWP importen la función [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) mediante P/Invoke si son necesarios para acceder a otras propiedades de interfaz de red.

## <a name="related-topics"></a>Temas relacionados

Para obtener definiciones de la base de información de administración (MIB) para interfaces de red, vea [RFC 2863](https://tools.ietf.org/html/rfc2863).

Para las interfaces de red de NDIS en controladores de red, vea Interfaces de [red de NDIS.](/windows-hardware/drivers/network/ndis-network-interfaces2)

Para obtener la referencia de la API netioapi.h, consulte [el encabezado netioapi.h](/windows/desktop/api/netioapi/).
