---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palabras clave públicas de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670095"
---
# <a name="printcapabilities-public-keywords"></a>Palabras clave públicas de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En la sección siguiente se especifican los elementos configurables por el usuario y las definiciones de parámetros que pueden ser aplicables a un documento de PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Uso de elementos configurables por el usuario

Los elementos configurables por el usuario representan palabras clave públicas del esquema de impresión que pueden aparecer en un documento de PrintCapabilities o en un PrintTicket. Están pensadas para representar atributos de dispositivo configurables admitidos por un dispositivo específico o comunicar el intento de impresión por parte de una aplicación o un usuario.

Los elementos configurables por el usuario pueden hacer referencia a elementos de referencia de parámetro. Para obtener más información, consulte la sección [elementos de referencia de parámetros](parameter-reference-elements.md) .

## <a name="parameter-definitions-usage"></a>Uso de definiciones de parámetros

Las definiciones de parámetros adoptan la forma de tipos de elementos ParameterDef en un documento de capacidades de impresión. Los tipos de elementos ParameterDef se inicializan en un PrintTicket mediante el tipo de elemento ParameterInit. El valor del parámetro se especificará mediante el elemento ParameterInit. Una palabra clave configurable por el usuario puede hacer referencia a una definición de parámetro mediante el tipo de elemento ParameterRef. Para obtener más información, consulte la sección [construcciones de parámetros](parameter-constructs.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



