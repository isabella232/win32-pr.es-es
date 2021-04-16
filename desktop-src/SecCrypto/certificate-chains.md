---
description: Para usar certificados para la seguridad, se debe comprobar la autenticidad y la validez de cada certificado recibido. Esta comprobación depende del concepto de confianza y la delegación del kit de \[ desarrollo de software (SDK) de plataforma de confianza \] .
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Cadenas de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea42b6788997a86aade6f89d0f35d92a74daafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497272"
---
# <a name="certificate-chains"></a>Cadenas de certificados

Para usar [*certificados*](../secgloss/c-gly.md) para la seguridad, se debe comprobar la autenticidad y la validez de cada certificado recibido. Esta comprobación depende del concepto de confianza y la delegación de confianza; para obtener más información, vea [jerarquía de confianza](hierarchy-of-trust.md).

Cada certificado contiene un campo de asunto que identifica el individuo o el grupo al que se emitió el certificado. Cada certificado también contiene un campo de emisor que identifica la [*entidad de certificación*](../secgloss/c-gly.md) (CA) habilitada para certificar la identidad del sujeto.

Una cadena de certificados consta de todos los certificados necesarios para certificar el sujeto identificado por el certificado final. En la práctica, esto incluye el certificado final, los certificados de las CA intermedias y el certificado de una entidad de certificación raíz de confianza para todas las partes de la cadena. Cada CA intermedia de la cadena contiene un certificado emitido por la CA un nivel por encima de él en la jerarquía de confianza. La entidad de certificación raíz emite un certificado para sí mismo.

El proceso de comprobación de la autenticidad y la validez de un certificado recién recibido implica la comprobación de todos los certificados de la cadena de certificados de la entidad de certificación original, de confianza universal, a través de las CA intermedias, hasta el certificado recién recibido, que se denomina el certificado final. Un nuevo certificado solo puede ser de confianza si cada certificado de la cadena de ese certificado se emite correctamente y es válido.

El seguimiento de todos los certificados que respaldan un nuevo certificado final puede resultar complicado. Por lo tanto, la tecnología [*CryptoAPI*](../secgloss/c-gly.md) 2,0 proporciona funciones que automatizan la creación de la cadena de certificados que respaldan cualquier certificado final determinado. Estas funciones también comprueban e informan sobre la validez de cada certificado en una cadena.

Las funciones de creación y comprobación de cadenas de [*CryptoAPI*](../secgloss/c-gly.md) 2,0 usan un motor de cadena para crear y comprobar cadenas de certificados. Un motor de cadena define un espacio de nombres de almacén y la partición de caché para la infraestructura de encadenamiento de certificados. CryptoAPI 2.0 proporciona un motor de cadena predeterminado para cualquier proceso de aplicación que solo use almacenes del sistema predeterminados (por ejemplo, MY, root, CA y Trust) para la creación de cadenas y el almacenamiento en caché. Una aplicación puede definir su propio espacio de nombres del almacén o tener su propia memoria caché con particiones creando su propio motor de cadena. Para lograr un comportamiento óptimo del almacenamiento en caché, se recomienda crear un motor de cadena único en el inicio de la aplicación y usar ese motor de cadena a lo largo de la duración de la aplicación.

Para obtener una lista de funciones, consulte funciones de comprobación de la [cadena de certificados](cryptography-functions.md). Si se trata de un programa que compila cadenas de certificados y comprueba los certificados, vea el [ejemplo C programa: crear una cadena de certificados](example-c-program-creating-a-certificate-chain.md).

 

 
