---
description: Obtenga información sobre los elementos configurables por el usuario y las definiciones de parámetros que pueden ser aplicables a un documento PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palabras clave públicas de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cccfa2cb22d8e784e8d4b82e548b9f4ae9772d1bd216573f5229d00f2f6d633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600625"
---
# <a name="printcapabilities-public-keywords"></a>Palabras clave públicas de PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En la sección siguiente se especifican los elementos configurables por el usuario y las definiciones de parámetros que pueden ser aplicables a un documento PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Uso de elementos configurables por el usuario

Los elementos configurables por el usuario representan palabras clave públicas del esquema de impresión que pueden aparecer en un documento PrintCapabilities o printTicket. Están diseñados para representar atributos de dispositivo configurables admitidos por un dispositivo específico o comunicar la intención de configuración de impresión por parte de una aplicación o usuario.

Los elementos configurables por el usuario pueden hacer referencia a elementos de referencia de parámetros. Para obtener más información, consulte la sección [Elementos de referencia de](parameter-reference-elements.md) parámetros.

## <a name="parameter-definitions-usage"></a>Uso de definiciones de parámetros

Las definiciones de parámetros tienen la forma de tipos de elementos ParameterDef en un documento De capacidades de impresión. Los tipos de elemento ParameterDef se inicializan en printTicket mediante el tipo de elemento ParameterInit. El valor del parámetro se especificará mediante el elemento ParameterInit. Una palabra clave configurable por el usuario puede hacer referencia a una definición de parámetro mediante el tipo de elemento ParameterRef. Para obtener más información, consulte la sección [Construcciones de parámetros.](parameter-constructs.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



