---
description: Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Control de versiones de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe405a629ddc64f76535b33554509b1a6fca81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542443"
---
# <a name="tspi-versioning"></a>Control de versiones de TSPI

Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios. Estas nuevas versiones pueden crear nuevas definiciones, como para nuevas características, nuevos miembros en estructuras de datos y nuevos campos de bits. Por lo tanto, los números de versión son necesarios para indicar cómo interpretar varias estructuras de datos.

Para permitir la interoperabilidad óptima de las distintas versiones de aplicaciones, versiones de TAPI propiamente dichas y versiones de proveedores de servicios de diferentes proveedores, la telefonía de Microsoft proporciona un mecanismo de negociación de la versión simple para las aplicaciones. En TAPI y el proveedor de servicios de telefonía para cada dispositivo de línea se deben acordar dos versiones diferentes. El primero es el número de versión del SPI de telefonía básico y complementario, denominado versión de la *interfaz TSPI*. El otro es para las extensiones específicas del proveedor, si existen, y se conoce como la *versión* de la extensión. El formato de las estructuras de datos y los tipos de datos que usan las características básicas y complementarias de TSPI se define mediante la versión de TSPI, mientras que la versión de la extensión determina el formato de las estructuras de datos definidas por las extensiones específicas del proveedor.

Estos dos tipos de negociación de versión se controlan mediante dos procedimientos diferentes: [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) se usa para negociar la versión de la interfaz TSPI y [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) se usa para negociar la versión de la extensión. La negociación de la versión de la extensión se puede omitir si no se desean extensiones. Si estos intervalos entran en la superposición de la negociación, el proveedor de servicios debe devolver un valor dentro de la parte que se superpone del intervalo como resultado de la negociación. Normalmente, debe ser el valor más alto posible. Si los intervalos no se superponen, las dos partes son incompatibles y la función devuelve un error.

Los resultados de una negociación simplemente indican que el proveedor de servicios está dispuesto a operar en un número de versión determinado, pero no confirma el proveedor de servicios para hacerlo. Por ejemplo, TAPI puede volver a negociar para determinar una versión ideal después de haber negociado una versión posible. La versión de la interfaz TSPI solo se confirma cuando se abre una línea con [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) y sobrevive hasta que se cierra el dispositivo. La versión de la extensión se confirma cuando se llama a la función [**\_ LineSelectExtVersion de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) y sobrevive hasta que la selección se cancela seleccionando la versión de extensión cero.

La selección de la versión de la extensión puede producirse muchas veces, incluso mientras está en vigor una versión de la extensión. Dado que el proveedor de servicios se confirma con la versión de la extensión, su intervalo de versiones admitidas se restringe exactamente a esa versión de la extensión. Por ejemplo, considere un proveedor de servicios que normalmente es compatible con las versiones de extensión de 1,0 a 5,5. Si la versión 3,0 está en vigor mientras un llamador intenta negociar una versión en el intervalo comprendido entre 1,0 y 5,5, la negociación devuelve 3,0.

Dado que TAPI negocia la versión, puede actualizar un proveedor de servicios a nuevas versiones de la interfaz sin necesidad de actualizar también TAPI. Del mismo modo, se puede actualizar TAPI, pero todavía se puede usar el proveedor de servicios anterior.

 

 
