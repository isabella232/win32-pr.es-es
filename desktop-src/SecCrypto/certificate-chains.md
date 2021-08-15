---
description: Para usar certificados por motivos de seguridad, se debe comprobar la autenticidad y validez de cada certificado recibido. Esta comprobación depende del concepto de confianza y la delegación de confianza del Kit de desarrollo de \[ software (SDK) de \] plataforma.
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Cadenas de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6efdd49cbd66c74805cc560286e5f15a981ef200df5523c602c2bb4b395a04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771944"
---
# <a name="certificate-chains"></a>Cadenas de certificados

Para usar [*certificados por*](../secgloss/c-gly.md) motivos de seguridad, se debe comprobar la autenticidad y validez de cada certificado recibido. Esta comprobación depende del concepto de confianza y la delegación de confianza. Para obtener más información, vea [Hierarchy of Trust](hierarchy-of-trust.md).

Cada certificado contiene un campo de asunto que identifica el individuo o grupo al que se emitió el certificado. Cada certificado también contiene un campo [](../secgloss/c-gly.md) de emisor que identifica la entidad de certificación (CA) capacitada para certificar la identidad del sujeto.

Una cadena de certificados consta de todos los certificados necesarios para certificar el sujeto identificado por el certificado final. En la práctica, esto incluye el certificado final, los certificados de entidades de certificación intermedias y el certificado de una CA raíz de confianza para todas las partes de la cadena. Cada CA intermedia de la cadena contiene un certificado emitido por la CA un nivel por encima de él en la jerarquía de confianza. La ca raíz emite un certificado por sí misma.

El proceso de comprobar la autenticidad y validez de un certificado recién recibido implica comprobar todos los certificados de la cadena de certificados de la CA original y de confianza universal, a través de cualquier CA intermedia, hasta el certificado que acaba de recibir, que se denomina certificado final. Solo se puede confiar en un certificado nuevo si cada certificado de la cadena de ese certificado se emite correctamente y es válido.

El seguimiento de todos los certificados que resalte un nuevo certificado final puede resultar complicado. Por lo tanto, la tecnología [*CryptoAPI*](../secgloss/c-gly.md) 2.0 proporciona funciones que automatizan la creación de la cadena de certificados que devuelven un certificado final determinado. Estas funciones también comprueban e informan sobre la validez de cada certificado de una cadena.

Las funciones de creación y comprobación de cadenas de [*CryptoAPI*](../secgloss/c-gly.md) 2.0 usan un motor de cadena para crear y comprobar cadenas de certificados. Un motor de cadena define un espacio de nombres de almacén y la creación de particiones de caché para la infraestructura de encadenamiento de certificados. CryptoAPI 2.0 proporciona un motor de cadena predeterminado para cualquier proceso de aplicación que solo use almacenes del sistema predeterminados (por ejemplo, MY, Root, CA y Trust) para la creación y el almacenamiento en caché de cadenas. Una aplicación puede definir su propio espacio de nombres de almacén o tener su propia caché con particiones mediante la creación de su propio motor de cadena. Para lograr un comportamiento óptimo del almacenamiento en caché, se recomienda crear un único motor de cadena al iniciar la aplicación y usar ese motor de cadena a lo largo de la duración de la aplicación.

Para obtener una lista de funciones, vea [Funciones de comprobación de la cadena de certificados](cryptography-functions.md). Para obtener un programa que compile cadenas de certificados y compruebe los certificados, vea Programa C de [ejemplo: Crear una cadena de certificados](example-c-program-creating-a-certificate-chain.md).

 

 
