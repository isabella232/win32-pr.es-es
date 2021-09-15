---
description: La interfaz del proveedor de servicios de seguridad (SSPI) proporciona una interfaz universal estándar del sector para aplicaciones distribuidas seguras.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Proveedores de servicios de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473656"
---
# <a name="security-service-providers"></a>Proveedores de servicios de seguridad

La interfaz del proveedor de servicios de seguridad (SSPI) proporciona una interfaz universal estándar del sector para aplicaciones distribuidas seguras. Peer Graphing API proporciona una manera para que las aplicaciones protejan vínculos en un grafo mediante la especificación de un proveedor de servicios de seguridad (SSP), que es un archivo DLL que implementa una interfaz SSPI. Una aplicación especifica un SSP cuando crea un grafo mediante [**PeerGraphCreate.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)

Para obtener más información sobre cómo crear su propio SSP, vea el vínculo de documentación de SSPI en la lista de vínculos de [referencia de graphing](graphing-reference-links.md).

## <a name="programming-considerations-for-implementing-an-ssp"></a>Consideraciones de programación para implementar un SSP

Tenga cuidado al llamar a una aplicación desde un SSP. Las consideraciones siguientes se aplican a las devoluciones de llamada de SSP:

-   Las devoluciones de llamada no deben tardar mucho tiempo en devolverse, porque se llaman durante la negociación de la conexión. Si una conexión tarda demasiado tiempo en establecerse, se puede descartar la conexión.
-   Peer Graphing API ajusta dinámicamente los valores de tiempo de espera de conexión, en función de la carga real de un sistema. El valor de tiempo de espera más bajo es de 20 segundos.
-   Para evitar posibles situaciones de interbloqueo, una aplicación no debe tener acceso a la base de datos de grafos del mismo nivel desde una devolución de llamada. Si una aplicación requiere información de la base de datos de grafos, la aplicación puede almacenar en caché la información necesaria y, a continuación, hacer referencia a la memoria caché desde dentro de la devolución de llamada. El almacenamiento en caché también puede ayudar a reducir el tiempo de conexión.

Al llamar a los puntos de entrada de SSPI, la infraestructura de grafos del mismo nivel requiere valores específicos para parámetros específicos de cinco (5) funciones. No puede cambiar estos valores de parámetro proporcionados a SSP y el SSP puede omitir los valores de los cinco parámetros o controlarlos correctamente. En la lista siguiente se identifican estos parámetros específicos y los valores necesarios:

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Especifique uno (1) para el *parámetro pvGetKeyArgument.* Especifica **NULL para** los parámetros *pszPrincipal,* *pvLogonID* y *pGetKeyFn.*

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Especifique las marcas siguientes para el parámetro *fContextReq:* **ISC \_ REQ \_ MUTUAL \_ AUTH \| ISC \_ REQ \_ CONFIDENTIALITY \| ISC \_ REQ \_ INTEGRITY ISC REQ SEQUENCE \| DETECT \_ \_ \_ \| ISC \_ REQ STREAM \_ \| ISC \_ REQ ALLOCATE \_ \_ MEMORY**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Especifique las marcas siguientes para el parámetro *fContextReq:* **ASC \_ REQ \_ MUTUAL \_ AUTH \| ASC \_ REQ \_ CONFIDENTIALITY \| ASC \_ REQ \_ INTEGRITY ASC REQ SEQUENCE \| DETECT \_ \_ \_ \| ASC \_ REQ STREAM \_ \| ASC \_ REQ \_ \_ ALLOCATE MEMORY**.

-   [**EncryptMessage**](graphing-reference-links.md)

    Especifique cero (0) para los *parámetros fQOP* *y MessageSeqNo.*

-   [**DecryptMessage**](graphing-reference-links.md)

    Especifique cero (0) para el *parámetro MessageSeqNo* y **NULL** para el *parámetro pfQOP.*

Al llamar [**a EncryptMessage**](graphing-reference-links.md), se pasan cuatro búferes en la **estructura SecBufferDesc.** En la tabla siguiente se identifica el orden para pasar los búferes.

| Estructura específica de SSP         | Descripción                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECBUFFER \_ STREAM \_ HEADER**  | Contiene los datos del encabezado de seguridad. El tamaño del búfer de encabezado se obtiene llamando a [**QueryContextAttributes**](graphing-reference-links.md) y especificando el atributo **SECPKG \_ ATTR \_ STREAM \_ SIZES.**  |
| **DATOS \_ SECBUFFER**            | Contiene el mensaje de texto sin formato que se va a cifrar.                                                                                                                                                                  |
| **FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER** | Contiene los datos del finalizador de seguridad. El tamaño del búfer de encabezado se obtiene llamando a [**QueryContextAttributes**](graphing-reference-links.md) y especificando el atributo **SECPKG \_ ATTR \_ STREAM \_ SIZES.** |
| **SECBUFFER \_ EMPTY**           | No inicializado. El tamaño de este búfer es cero (0).                                                                                                                                                             |



 

Al llamar [**a DecryptMessage**](graphing-reference-links.md), peer Graphing API pasa exactamente cuatro **estructuras SecBuffer.** El primer búfer es **SECBUFFER \_ DATA** y contiene un mensaje cifrado. Los búferes restantes se usan para la salida y son de tipo **SECBUFFER \_ EMPTY.**

El SSP debe admitir el cifrado y descifrado de búferes de datos de usuario con tamaños de 16K y superiores en una llamada.

 

 



