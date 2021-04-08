---
description: Para enviar datos a través de un medio de comunicación como una línea telefónica, los datos se deben serializar&\# 8212; es decir, se convierten en una cadena de unos y ceros que se transmiten en serie en la línea.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Datos codificados y descodificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b130232ac67503c6a20835c4c9b4e728b36f8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001050"
---
# <a name="encoded-and-decoded-data"></a>Datos codificados y descodificados

Para enviar datos a través de un medio de comunicación como una línea telefónica, los datos se deben [*serializar*](../secgloss/s-gly.md), es decir, se convierten en una cadena de unos y ceros que se transmiten en serie a través de la línea. La serialización debe realizarse de forma que el equipo que recibe los datos pueda volver a convertir los datos a su formato original. La forma en que se realiza la serialización se denomina [*Protocolo de comunicación*](../secgloss/c-gly.md)y se controla mediante el software y el hardware de transmisión de datos. Hay varios niveles en los que se convierten los datos. En la ilustración siguiente se muestra una vista muy simplificada de las capas del Protocolo de comunicación.

![capas de protocolo de comunicación](images/layer.png)

En la ilustración anterior se muestra el nivel de aplicación del equipo \# 1 que envía los datos que se van a transmitir (que normalmente constan de una combinación de caracteres de texto y números) a la capa de codificación y descodificación. La capa codificar/descodificar codifica los datos en un flujo de bytes del equipo. En el nivel más bajo, la capa de hardware, el hardware convierte los bytes de datos en una secuencia de serie de unos y ceros que se transmiten a través de la línea al equipo \# 2. La capa de hardware del equipo \# 2 convierte los datos y ceros en bytes del equipo y los pasa a la capa de codificación y descodificación para la descodificación. La capa codificar/descodificar descodifica los bytes de nuevo en su formato original y pasa los datos hasta el nivel de la aplicación.

Un principio de diseño de software aceptado es el uso de la *abstracción*, es decir, el proceso de describir un problema u objeto en lo que respecta a sus parámetros generales en lugar de describir todos los detalles necesarios para resolver el problema, o describir todos los detalles de un objeto. Mediante el uso de la abstracción, un diseñador puede especificar un objeto de software que tiene cualidades específicas sin preocuparse por el modo en que el objeto se implementa en el código de software. Esta práctica deja abierta la implementación. También simplifica la especificación y hace posible el estado axioms sobre el objeto que se puede demostrar cuando se implementa el objeto. Estos axioms se pueden suponer después cuando el objeto se emplea en otro objeto de nivel superior. La abstracción es el sello de la mayoría de las especificaciones de software moderna.

La mayoría de los [*protocolos de comunicación*](../secgloss/c-gly.md) implican una buena abstracción. Los objetos de niveles superiores se definen de forma abstracta y están diseñados para implementarse mediante objetos en capas inferiores. Por ejemplo, un servicio de una capa podría requerir la transferencia de determinados objetos abstractos entre equipos. Una capa de nivel inferior puede usar reglas de codificación para transformar los objetos abstractos en cadenas de unos y ceros.

Un método común para especificar objetos abstractos destinados a ser transmitidos en serie se denomina [*notación de sintaxis abstracta uno*](../secgloss/a-gly.md) (ASN. 1). ASN. 1 se define en la recomendación de CCITt [*X. 208*](../secgloss/x-gly.md). Un conjunto de reglas ASN. 1 para representar dichos objetos como cadenas de unos y ceros se denomina [*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) y se define en la recomendación de CCITT [*X. 509*](../secgloss/x-gly.md), sección 8,7. Estos son los métodos de codificación que usa actualmente CryptoAPI.

Para obtener más información acerca de las funciones de [codificación y descodificación, consulte funciones para codificar y descodificar objetos](cryptography-functions.md).

 

 
