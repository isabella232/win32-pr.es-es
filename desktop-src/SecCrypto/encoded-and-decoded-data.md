---
description: Para enviar datos a través de un medio de comunicación como una línea telefónica, los datos se deben serializar&8212; es decir, se convierten en una cadena de unos y ceros que se transmiten en serie a través de la \# línea.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Datos codificados y descodificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b130232ac67503c6a20835c4c9b4e728b36f8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476458"
---
# <a name="encoded-and-decoded-data"></a>Datos codificados y descodificados

Para enviar datos a través de un medio de [](../secgloss/s-gly.md)comunicación como una línea telefónica, los datos se deben serializar, es decir, se deben convertir en una cadena de unos y ceros que se transmiten en serie a través de la línea. La serialización debe realizarse de forma que el equipo que recibe los datos pueda volver a convertir los datos a su formato original. La forma en que se realiza la serialización se denomina protocolo [*de comunicación*](../secgloss/c-gly.md)y se controla mediante software y hardware de transmisión de datos. Hay varios niveles en los que se convierten los datos. En la ilustración siguiente se muestra una vista muy simplificada de las capas del protocolo de comunicación.

![capas de protocolo de comunicación](images/layer.png)

En la ilustración anterior se muestra la capa de aplicación en el equipo 1 que envía los datos que se transmiten (que normalmente consta de una combinación de caracteres textuales y números) a la capa de codificación y \# descodificación. La capa de codificación y descodificación codifica los datos en una secuencia de bytes del equipo. En el nivel más bajo, la capa de hardware, el hardware convierte los bytes de datos en una secuencia serie de unos y ceros que se transmite a través de la línea al equipo \# 2. La capa de hardware del equipo 2 convierte los valores de uno y ceros en bytes del equipo y los pasa a la capa de codificación y descodificación para \# descodificarlos. La capa de codificación y descodificación descodifica los bytes de nuevo en su formato original y pasa los datos a la capa de aplicación.

Un principio de diseño de software aceptado es usar la *abstracción*, es decir, el proceso de describir un problema u objeto en términos de sus parámetros generales en lugar de describir todos los detalles necesarios para resolver el problema o describir todos los detalles de un objeto. Mediante la abstracción, un diseñador puede especificar un objeto de software que tenga calidades específicas sin preocuparse de cómo se implementa realmente el objeto en el código de software. Este procedimiento deja abierta la implementación. También simplifica la especificación y permite establecer axiomas sobre el objeto que se puede demostrar cuando se implementa el objeto. Estos axiomas se pueden asumir cuando el objeto se emplea en otro objeto de nivel superior. La abstracción es el distintivo de la mayoría de las especificaciones de software más modernas.

La [*mayoría de los protocolos*](../secgloss/c-gly.md) de comunicación implican una gran cantidad de abstracción. Los objetos de capas superiores se definen abstractamente y están diseñados para implementarse mediante objetos en capas inferiores. Por ejemplo, un servicio de una capa puede requerir la transferencia de determinados objetos abstractos entre equipos. Una capa de nivel inferior puede usar reglas de codificación para transformar los objetos abstractos en cadenas de uno y ceros.

Un método común para especificar objetos abstractos destinados a transmitirse en serie se denomina [*Notation One*](../secgloss/a-gly.md) de sintaxis abstracta (ASN.1). ASN.1 se define en la recomendación [*X.208*](../secgloss/x-gly.md)de CC RECOMMENDATION. Un conjunto de reglas de ASN.1 para representar tales objetos como cadenas de uno y ceros se denomina [*reglas de codificación distinguida*](../secgloss/d-gly.md) (DER) y se define en la recomendación [*X.509*](../secgloss/x-gly.md)de CC RECOMMENDATION, sección 8.7. Estos son los métodos de codificación usados actualmente por CryptoAPI.

Para obtener más información sobre las funciones de codificación y descodificación, vea Codificación de objetos y [Funciones de descodificación](cryptography-functions.md).

 

 
