---
description: Un certificado X.509 versión 2 contiene los campos básicos definidos en la versión 1 y, además, agrega los siguientes campos.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Campos de la versión 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7aed470acfbc3c9a648de46f89a72dc3de361e61eed39cdce4aebbf28e133f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903431"
---
# <a name="version-2-fields"></a>Campos de la versión 2

Un certificado X.509 versión 2 contiene los campos básicos definidos en la versión 1 y, además, agrega los siguientes campos.

## <a name="issuer-unique-identifier"></a>Identificador único de emisor

Contiene un valor único que se puede utilizar para hacer que el nombre X.500 de la CA no sea ambiguo si lo reutilizan distintas entidades a lo largo del tiempo.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>Identificador único de firmante

Contiene un valor único que se puede utilizar para hacer que el nombre X.500 del firmante del certificado no sea ambiguo si lo reutilizan distintas entidades a lo largo del tiempo.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Campos básicos](about-basic-fields.md)
</dt> <dt>

[Extensiones de la versión 3](about-version-3-extensions.md)
</dt> <dt>

[Certificados de clave pública X.509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



