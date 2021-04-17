---
description: La interfaz del proveedor de servicios de seguridad (SSPI) proporciona una interfaz universal estándar del sector para aplicaciones distribuidas seguras.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Proveedores de servicios de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668056"
---
# <a name="security-service-providers"></a>Proveedores de servicios de seguridad

La interfaz del proveedor de servicios de seguridad (SSPI) proporciona una interfaz universal estándar del sector para aplicaciones distribuidas seguras. La API de gráficos del mismo nivel proporciona a las aplicaciones una manera de proteger los vínculos de un gráfico mediante la especificación de un proveedor de servicios de seguridad (SSP), que es un archivo DLL que implementa una interfaz SSPI. Una aplicación especifica un SSP cuando crea un grafo con [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).

Para obtener más información sobre la creación de su propio SSP, consulte el vínculo de documentación de SSPI en la lista de [vínculos de referencia de gráficos](graphing-reference-links.md).

## <a name="programming-considerations-for-implementing-an-ssp"></a>Consideraciones de programación para implementar un SSP

Tenga cuidado al llamar a una aplicación desde dentro de un SSP. Las siguientes consideraciones se aplican a las devoluciones de llamada de SSP:

-   Las devoluciones de llamada no deben tardar mucho tiempo en devolverse, porque se llama durante la negociación de la conexión. Si tarda demasiado tiempo en establecerse una conexión, la conexión se puede quitar.
-   La API de gráficos del mismo nivel ajusta dinámicamente los valores de tiempo de espera de conexión, en función de la carga real de un sistema. El valor de tiempo de espera más bajo es de 20 segundos.
-   Para evitar posibles situaciones de interbloqueo, una aplicación no debe tener acceso a la base de datos de gráficos del mismo nivel desde una devolución de llamada. Si una aplicación requiere información de la base de datos de gráficos, la aplicación puede almacenar en caché la información necesaria y, a continuación, hacer referencia a la memoria caché desde dentro de la devolución de llamada. El almacenamiento en caché también puede ayudar a reducir el tiempo de conexión.

Al llamar a los puntos de entrada SSPI, la infraestructura de gráficos del mismo nivel requiere valores específicos para parámetros específicos de cinco (5) funciones. No se pueden cambiar estos valores de parámetro proporcionados por SSP y el SSP puede omitir los valores de los cinco parámetros o controlarlos correctamente. En la lista siguiente se identifican estos parámetros específicos y los valores necesarios:

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Especifique un (1) para el parámetro *pvGetKeyArgument* . Especifica **null** para los parámetros *pszPrincipal*, *pvLogonID* y *pGetKeyFn* .

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Especifique las marcas siguientes para el parámetro *fContextReq* : **ISC \_ req \_ Mutual \_ auth \| ISC req confidencialidad de ISC \_ \_ req Integrity de ISC req \| \_ \_ \| \_ \_ Sequence \_ detectar \| ISC \_ req Stream de \_ \| ISC \_ req \_ asignar \_ memoria**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Especifique las marcas siguientes para el parámetro *fContextReq* : ASC req **\_ \_ Mutual \_ auth \| ASC \_ req \_ confidencialidad \| ASC \_ req secuencia de \_ \| \_ solicitud \_ \_ \| \_ \_ \| \_ \_ \_** de solicitud de inversión de ASC req Stream req solicitud de asignación de memoria.

-   [**EncryptMessage**](graphing-reference-links.md)

    Especifique cero (0) para los parámetros *fQOP* y *MessageSeqNo* .

-   [**DecryptMessage**](graphing-reference-links.md)

    Especifique cero (0) para el parámetro *MessageSeqNo* y **null** para el parámetro *pfQOP* .

Al llamar a [**EncryptMessage**](graphing-reference-links.md), se pasan cuatro búferes en la estructura **SecBufferDesc** . En la tabla siguiente se identifica el orden de pasar los búferes.

| Estructura específica de SSP         | Descripción                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECBUFFER \_ encabezado de secuencia \_**  | Contiene los datos del encabezado de seguridad. El tamaño del búfer de encabezado se obtiene llamando a [**QueryContextAttributes**](graphing-reference-links.md) y especificando el atributo **SECPKG \_ ATTR \_ Stream \_ sizes** .  |
| **datos de SECBUFFER \_**            | Contiene el mensaje de texto sin formato que se va a cifrar.                                                                                                                                                                  |
| **\_finalizador de flujo SECBUFFER \_** | Contiene los datos del finalizador de seguridad. El tamaño del búfer de encabezado se obtiene llamando a [**QueryContextAttributes**](graphing-reference-links.md) y especificando el atributo **SECPKG \_ ATTR \_ Stream \_ sizes** . |
| **SECBUFFER \_ vacío**           | No inicializado. El tamaño de este búfer es cero (0).                                                                                                                                                             |



 

Al llamar a [**DecryptMessage**](graphing-reference-links.md), la API de gráficos del mismo nivel pasa exactamente cuatro estructuras **SecBuffer** . El primer búfer es **SECBUFFER \_ Data** y contiene un mensaje cifrado. Los búferes restantes se utilizan para la salida y son del tipo **SECBUFFER \_ vacío**.

El SSP debe admitir el cifrado y descifrado de los búferes de datos de usuario con tamaños de 16 k y mayores en una llamada.

 

 



