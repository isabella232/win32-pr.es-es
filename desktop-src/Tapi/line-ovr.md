---
description: El concepto de línea ha evolucionado a lo largo del tiempo y se ha sustituido en parte por los conceptos de dirección y terminal. TAPI 3 no usa directamente el concepto de línea, pero TAPI 2 continúa incorporando este paradigma.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8275555e0cb34f5831ce671e22a89a1499fb1796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556385"
---
# <a name="line"></a>Línea

El concepto de línea ha evolucionado a lo largo del tiempo y se ha sustituido en parte por los conceptos de dirección y terminal. TAPI 3 no usa directamente el concepto de línea, pero TAPI 2 continúa incorporando este paradigma.

Un *dispositivo de línea* es un dispositivo físico, como un panel de fax, un módem o una tarjeta ISDN (RDSI) que está conectada a una red. Es posible que el dispositivo no esté conectado físicamente al equipo en el que se ejecuta la aplicación TAPI, como un grupo de módems en un servidor. Los dispositivos de línea admiten capacidades de comunicaciones al permitir que las aplicaciones envíen o reciban información de una red. Un dispositivo de línea contiene un conjunto de uno o más canales homogéneos que se pueden utilizar para establecer llamadas.

En las aplicaciones TAPI 2. x, un dispositivo de línea es la representación lógica de un dispositivo telefónico físico. Aunque "line" suele indicar algo con dos puntos de conexión, es posible abstraer un dispositivo de línea en un único punto porque TAPI solo lo ve como un punto de entrada a la línea que conduce al conmutador.

![dispositivos de línea](images/ch0501.png)

Aunque las tres líneas de la ilustración anterior se componen de hardware diferente y se usan para distintas funciones, se abstraen en el mismo tipo de dispositivo y se rigen por las mismas reglas. El teléfono no representa un dispositivo de teléfono, sino un dispositivo de línea usado para las llamadas de voz. Cuando se usa este dispositivo de línea para llamadas entrantes o salientes, la aplicación también necesita abrir y controlar una instancia de la clase de dispositivo de teléfono, que se describe en detalle en secciones posteriores.

La clase de dispositivo de línea es una representación independiente del dispositivo de un dispositivo de línea física, como un módem. Puede contener uno o más canales de comunicaciones idénticos (que se usan para la señalización o la información) entre la aplicación y el conmutador o la red. Dado que los canales que pertenecen a una sola línea tienen funcionalidades idénticas, son intercambiables. En muchos casos (como en el caso de los POTS), un proveedor de servicios modelará una línea como si tuviera un solo canal. Otras tecnologías, como ISDN, ofrecen más canales y el proveedor de servicios debe tratarlas en consecuencia.

**TAPI 2. x:** Las aplicaciones detectan funcionalidades de línea mediante la función [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) . Se debe haber llamado previamente a la negociación de la versión mediante las funciones [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) de [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) .

**TAPI 3. x:** Las aplicaciones dependen principalmente del concepto de dirección.

 

 
