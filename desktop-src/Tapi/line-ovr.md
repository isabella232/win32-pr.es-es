---
description: El concepto de línea ha evolucionado con el tiempo y se ha reemplazado parcialmente por los conceptos de dirección y terminal. TAPI 3 no usa directamente el concepto de línea, pero TAPI 2 sigue incorporando este paradigma.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c299924a69d3e6e4889d14a72a571ca11ed2dc9e97514702f8ba4836f4c5b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660214"
---
# <a name="line"></a>Línea

El concepto de línea ha evolucionado con el tiempo y se ha reemplazado parcialmente por los conceptos de dirección y terminal. TAPI 3 no usa directamente el concepto de línea, pero TAPI 2 sigue incorporando este paradigma.

Un *dispositivo de línea* es un dispositivo físico, como una placa de fax, un módem o una tarjeta ISDN que está conectada a una red. Es posible que el dispositivo no esté conectado físicamente al equipo en el que se ejecuta la aplicación TAPI, como un grupo de módems en un servidor. Los dispositivos de línea admiten funcionalidades de comunicaciones al permitir que las aplicaciones envíen o reciban información de una red. Un dispositivo de línea contiene un conjunto de uno o varios canales homogéneos que se pueden usar para establecer llamadas.

Dentro de las aplicaciones TAPI 2.x, un dispositivo de línea es la representación lógica de un dispositivo telefónico físico. Aunque "línea" suele indicar algo con dos puntos de conexión, es posible abstraer un dispositivo de línea a un único punto porque TAPI lo ve solo como un punto de entrada a la línea que conduce al conmutador.

![dispositivos de línea](images/ch0501.png)

Aunque las tres líneas de la ilustración anterior se componen de hardware diferente y se usan para distintas funciones, se abstrae al mismo tipo de dispositivo y se rigen por las mismas reglas. El teléfono no representa un dispositivo de teléfono, sino un dispositivo de línea que se usa para las llamadas de voz. Al usar este dispositivo de línea para llamadas entrantes o salientes, la aplicación también tendría que abrir y controlar una instancia de la clase phone-device, que se describe en detalle en secciones posteriores.

La clase de dispositivo line es una representación independiente del dispositivo de un dispositivo de línea física, como un módem. Puede contener uno o varios canales de comunicaciones idénticos (que se usan para la señalización o la información) entre la aplicación y el conmutador o la red. Dado que los canales que pertenecen a una sola línea tienen funcionalidades idénticas, son intercambiables. En muchos casos (como con POTS), un proveedor de servicios modela una línea como que solo tiene un canal. Otras tecnologías, como ISDN, ofrecen más canales y el proveedor de servicios debe tratarlos en consecuencia.

**TAPI 2.x:** Las aplicaciones detectan funcionalidades de línea [**mediante la función lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) Se debe haber llamado previamente a la negociación de versiones mediante las funciones [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion.**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion)

**TAPI 3.x:** Las aplicaciones se basan principalmente en el concepto de dirección.

 

 
