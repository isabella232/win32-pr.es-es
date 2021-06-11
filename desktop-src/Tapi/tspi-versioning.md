---
description: Obtenga información sobre el control de versiones de TSPI. Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Control de versiones de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0a0663a1fcc685df8643c634ec627f669aafe8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989240"
---
# <a name="tspi-versioning"></a>Control de versiones de TSPI

Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios. Estas nuevas versiones pueden crear nuevas definiciones, como para nuevas características, nuevos miembros en estructuras de datos y nuevos campos de bits. Por lo tanto, los números de versión son necesarios para indicar cómo interpretar varias estructuras de datos.

Para permitir una interoperabilidad óptima de diferentes versiones de aplicaciones, versiones de TAPI propiamente dichas y versiones de proveedores de servicios por parte de distintos proveedores, Microsoft Telefonía proporciona un mecanismo de negociación de versiones simple para las aplicaciones. TapI y el proveedor de servicios de telefonía deben acordar dos versiones diferentes para cada dispositivo de línea. El primero es el número de versión del SPI de telefonía básica y complementaria, denominado versión *de la interfaz TSPI.* El otro es para extensiones específicas del proveedor, si las hay, y se conoce como la versión *de extensión*. El formato de las estructuras de datos y los tipos de datos utilizados por las características Básica y Complementaria de TSPI se define mediante la versión de TSPI, mientras que la versión de la extensión determina el formato de las estructuras de datos definidas por las extensiones específicas del proveedor.

Estos dos tipos de negociación de versiones se controlan mediante dos procedimientos diferentes: la línea [**\_ TSPINegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) se usa para negociar la versión de la interfaz TSPI y la línea [**\_ TSPINegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) se usa para negociar la versión de la extensión. La negociación de la versión de extensión se puede omitir si no se quieren extensiones. Si estos intervalos se superponen durante la negociación, el proveedor de servicios debe devolver un valor dentro de la parte superpuesta del intervalo como resultado de la negociación. Normalmente, debe ser el valor más alto posible. Si los intervalos no se superponen, las dos partes son incompatibles y la función devuelve un error.

Los resultados de una negociación simplemente indican que el proveedor de servicios está dispuesto a funcionar con un número de versión determinado, pero no se compromete a hacerlo. Por ejemplo, TAPI puede renegociar para determinar una versión ideal después de haber negociado una versión posible. La versión de la interfaz TSPI solo se confirma cuando se abre una línea mediante la línea [**\_ TSPIAbrir**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) y sobrevive hasta que se cierra el dispositivo. La versión de extensión se confirma cuando se llama a la función [**\_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) de TSPI y sobrevive hasta que se cancela la selección seleccionando la versión cero de la extensión.

La selección de la versión de la extensión puede producirse muchas veces, incluso mientras una versión de extensión está en vigor. Dado que el proveedor de servicios está confirmado en la versión de la extensión, su intervalo de versiones admitidas se limita exactamente a esa versión de extensión. Por ejemplo, considere un proveedor de servicios que normalmente sea compatible con las versiones de extensión 1.0 a 5.5. Si la versión 3.0 está en vigor mientras un autor de la llamada intenta negociar una versión dentro del intervalo de 1.0 a 5.5, la negociación devuelve 3.0.

Dado que TAPI negocia la versión, puede actualizar un proveedor de servicios a nuevas versiones de la interfaz sin necesidad de actualizar también TAPI. Del mismo modo, TAPI se puede actualizar, pero seguir utilizando el proveedor de servicios anterior.

 

 
