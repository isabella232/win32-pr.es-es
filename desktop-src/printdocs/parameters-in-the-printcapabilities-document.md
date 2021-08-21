---
description: Comprenda los parámetros del documento PrintCapabilities. Este tema no está al día. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parámetros del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a2d88e75372cfc2f1301c630116c12510b37c91aadbf94a04ac07a3f4906cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867997"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parámetros del documento PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Como se describe en [Elementos](parameter-reference-elements.md)de referencia de parámetros , se puede hacer referencia a los elementos ParameterInit desde instancias de Option, pero la construcción de parámetros también tiene un uso que es independiente de este tipo de elemento.

Un ejemplo de un atributo de configuración de dispositivo que es adecuado para la representación de parámetros es CopyCount. Los valores permitidos para este atributo de configuración de dispositivo se pueden definir de forma fácil y concisa sin enumerar cada uno de ellos explícitamente. Aunque sería posible, aunque tedioso, enumerar cada valor copyCount en su propia opción, algunos atributos de configuración de dispositivo simplemente no se pueden representar mediante una construcción característica/opción. Por ejemplo, considere un dispositivo que acepta una cadena de texto que luego se usa para generar una marca de agua virtual en cada página de salida. El conjunto de todas las cadenas de texto posibles no se puede enumerar explícitamente fácilmente, pero la cadena de texto se puede describir fácilmente mediante un elemento ParameterDef.

El documento Palabras clave de esquema de impresión define una serie de construcciones de parámetros que se usan habitualmente, pero los proveedores printCapabilities pueden definir otras adicionales. Sin embargo, estas construcciones de parámetros definidas de forma privada no son portátiles para otros dispositivos, debido al hecho de que un documento PrintCapabilities proporcionado por otra parte no define dicha construcción de parámetros. Tanto si el esquema está definido como si está definido de forma privada, la instancia de ParameterDef debe estar presente en el documento PrintCapabilities antes de que los clientes reconozcan y usen el parámetro. Estos parámetros se conocen como *parámetros designados.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



