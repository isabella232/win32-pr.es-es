---
description: El campo Longitud de un triplete TLV identifica el número de bytes codificados en el campo Valor.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Bytes de longitud y valor codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160750"
---
# <a name="encoded-length-and-value-bytes"></a>Bytes de longitud y valor codificados

El *campo* Longitud de un triplete TLV identifica el número de bytes codificados en el *campo* Valor. El *campo* Valor contiene el contenido que se envía entre equipos. Si el *campo* Valor contiene menos de 128 bytes, el *campo Longitud* solo requiere un byte. El bit 7 del *campo Longitud* es cero (0) y los bits restantes identifican el número de bytes de contenido que se envía. Si el *campo Valor* contiene más de 127  bytes, el bit 7 del campo Longitud es uno (1) y los bits restantes identifican el número de bytes necesarios para contener la longitud. En la ilustración siguiente se muestran ejemplos.

![byte de longitud der tlv](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de transferencia de DER](about-der-transfer-syntax.md)
</dt> <dt>

[Bytes de etiqueta codificados](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



