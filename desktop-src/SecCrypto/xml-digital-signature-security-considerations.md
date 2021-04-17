---
description: Las aplicaciones que firman y comprueban las firmas digitales XML se deben escribir de acuerdo con las siguientes prácticas recomendadas para evitar ataques de denegación de servicio, pérdida de datos y riesgo de información privada.
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: Consideraciones de seguridad de las firmas digitales XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e54b4c5f3f863e0bc84172a7507bfe8609e2df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688180"
---
# <a name="xml-digital-signature-security-considerations"></a>Consideraciones de seguridad de las firmas digitales XML

Las aplicaciones que firman y comprueban las firmas digitales XML se deben escribir de acuerdo con las siguientes prácticas recomendadas para evitar ataques de denegación de servicio, pérdida de datos y riesgo de información privada. La siguiente lista proporciona instrucciones generales; sin embargo, se recomienda a los desarrolladores que realicen análisis de seguridad adicionales específicos de sus aplicaciones y revisen los procedimientos recomendados de firmas digitales más recientes publicados por el W3C.

-   [Comprobar la confianza de la clave de firma](#verify-trust-of-the-signing-key)
-   [Compruebe primero la clave de firma y valide SignedInfo y, a continuación, valide las referencias](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [Usar el conjunto mínimo de algoritmos de canonización y transformaciones necesarias](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [Asegurarse de que los URI de destino apuntan a destinos dentro del ámbito esperado](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [Comprobar que la firma ha comprobado los datos consumidos por la aplicación](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [Siga las mejores prácticas criptográficas](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>Comprobar la confianza de la clave de firma

Asegúrese de que la clave de firma sea de confianza comprobando el certificado [*X. 509*](../secgloss/x-gly.md) correspondiente (y la cadena de certificados) incluido en el mensaje firmado. Como alternativa, la confianza en la clave de firma se puede establecer en un modo fuera de banda, como un administrador que configure un conjunto de claves de confianza o una aplicación que consulte un servicio de confianza a través de un canal seguro.

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>Compruebe primero la clave de firma y valide SignedInfo y, a continuación, valide las referencias

Compruebe la confianza en la clave de firma y la integridad del elemento **SignedInfo** antes de validar las referencias. Del mismo modo, las aplicaciones deben validar los elementos de **manifiesto** antes de resolver las referencias contenidas en los elementos de **manifiesto** . Los elementos de **referencia** permiten la especificación de URI de destino, transformaciones y algoritmos de canonización. Si no se valida, estos campos se pueden usar para crear denegación de servicio, pérdida de datos u otros ataques.

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>Usar el conjunto mínimo de algoritmos de canonización y transformaciones necesarias

XSLT y XPATH no se deben usar dentro de elementos no autenticados, como **KeyInfo**. Si una aplicación requiere el uso de XPath, restrinja el conjunto de expresiones XPATH permitidas para solo las que utilizan los ejes antecesores o propios y no calcule el valor de cadena de los elementos. De forma predeterminada, CryptXML admite un conjunto limitado de algoritmos de canonización (vea URI admitidos en [algoritmos criptográficos de firma digital XML](xml-digital-signature-cryptographic-algorithms.md)). Los desarrolladores pueden implementar transformaciones adicionales o algoritmos de canonización para su uso dentro de su aplicación. Sin embargo, el uso de algoritmos complejos crea la posibilidad de ataques de denegación de servicio o de las características de rechazo de una firma. En los casos en los que la aplicación requiera transformaciones, limite el número de transformaciones que se pueden especificar por referencia al número más alto requerido por la aplicación. Esta práctica mitiga los ataques de denegación de servicio en función del uso excesivo de las transformaciones.

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>Asegurarse de que los URI de destino apuntan a destinos dentro del ámbito esperado

Las aplicaciones deben limitar los URI de destino al ámbito más pequeño requerido por la aplicación. Por ejemplo, se espera que los URI apunten a los destinos del mismo documento, a los archivos de un directorio de destino específico o a ubicaciones de red dentro de un dominio DNS específico. Los URI establecidos por un atacante para que apunten fuera del dominio esperado pueden hacer que una aplicación recupere contenido malintencionado, envíe solicitudes HTTP malintencionadas (posiblemente con cadenas de consulta) o que las aplicaciones se autentiquen en servidores malintencionados.

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>Comprobar que la firma ha comprobado los datos consumidos por la aplicación

Si la aplicación valida la clave de firma y los elementos **SignedInfo** y **Reference** , pero la aplicación consume datos importantes a los que no hace referencia la firma, la firma no proporciona ninguna protección significativa. El significado semántico de una firma puede variar en función de la posición de la firma dentro del documento. Se recomienda que las aplicaciones comprueben la posición de la firma dentro de un documento. Además, Compruebe la posición de los nombres de elementos y datos a los que se hace referencia para mitigar los ataques de ajuste y sustitución.

## <a name="follow-best-cryptographic-practices"></a>Siga las mejores prácticas criptográficas

Los algoritmos criptográficos se vuelven más débiles con el tiempo a medida que se detectan nuevos ataques y se pone a disposición más potencia de computación. No codifique de forma rígida los identificadores o tamaños de clave de los algoritmos criptográficos en las aplicaciones. Para obtener una lista completa de las prácticas criptográficas más adecuadas, consulte Michael Howard y Steve Lipner, "estándares criptográficos mínimos de SDL", en *el ciclo de vida de desarrollo de seguridad* (Redmond, Washington: Microsoft Press, 2006), 251 – 258.

Se pueden encontrar prácticas recomendadas adicionales en el sitio web de W3C: https://www.w3.org .

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
