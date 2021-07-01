---
description: Comprenda los parámetros del documento PrintCapabilities. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parámetros del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118630"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parámetros del documento PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Como se describe en [Elementos](parameter-reference-elements.md)de referencia de parámetros , se puede hacer referencia a los elementos ParameterInit desde instancias de Option, pero la construcción de parámetros también tiene un uso que es independiente de este tipo de elemento.

Un ejemplo de un atributo de configuración de dispositivo que es adecuado para la representación de parámetros es CopyCount. Los valores permitidos para este atributo de configuración de dispositivo se pueden definir de forma fácil y concisa sin enumerar cada uno de ellos explícitamente. Aunque sería posible, aunque tedioso, enumerar cada valor copyCount en su propia opción, algunos atributos de configuración de dispositivo simplemente no se pueden representar mediante una construcción de característica o opción. Por ejemplo, considere un dispositivo que acepta una cadena de texto que luego se usa para generar una marca de agua virtual en cada página de salida. El conjunto de todas las cadenas de texto posibles no se puede enumerar explícitamente fácilmente, pero la cadena de texto se puede describir fácilmente mediante un elemento ParameterDef.

El documento Palabras clave de esquema de impresión define una serie de construcciones de parámetros usadas con frecuencia, pero los proveedores printCapabilities pueden definir otras adicionales propias. Sin embargo, estas construcciones de parámetros definidas de forma privada no son portátiles para otros dispositivos, debido al hecho de que un documento PrintCapabilities proporcionado por otra parte no define dicha construcción de parámetro. Ya sea definido por el esquema o definido de forma privada, la instancia de ParameterDef debe estar presente en el documento PrintCapabilities antes de que los clientes reconozcan y usen el parámetro. Estos parámetros se conocen como *parámetros designados.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



