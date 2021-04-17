---
description: El campo de longitud de un trío TLV identifica el número de bytes codificados en el campo de valor.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Bytes de valor y longitud codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666951"
---
# <a name="encoded-length-and-value-bytes"></a>Bytes de valor y longitud codificados

El campo de *longitud* de un trío TLV identifica el número de bytes codificados en el campo de *valor* . El campo *valor* contiene el contenido que se envía entre equipos. Si el campo de *valor* contiene menos de 128 bytes, el campo de *longitud* solo requiere un byte. El bit 7 del campo de *longitud* es cero (0) y los bits restantes identifican el número de bytes de contenido que se envía. Si el campo de *valor* contiene más de 127 bytes, el bit 7 del campo de *longitud* es uno (1) y los bits restantes identifican el número de bytes necesarios para contener la longitud. Los ejemplos se muestran en la siguiente ilustración.

![byte de longitud del TLV der](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de transferencia DER](about-der-transfer-syntax.md)
</dt> <dt>

[Bytes de etiqueta codificados](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



