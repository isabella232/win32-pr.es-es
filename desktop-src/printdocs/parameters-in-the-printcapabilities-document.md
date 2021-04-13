---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parámetros del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361965"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Parámetros del documento PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Como se describe en [elementos de referencia de parámetros](parameter-reference-elements.md), se puede hacer referencia a los elementos ParameterInit desde instancias de opciones, pero la construcción de parámetro también tiene un uso que es independiente de este tipo de elemento.

Un ejemplo de un atributo de configuración de dispositivo que está bien adaptado para la representación de parámetros es CopyCount. Los valores permitidos para este atributo de configuración de dispositivo pueden definirse de manera fácil y concisa sin enumerarlos explícitamente. Aunque sería posible, aunque tedioso, mostrar cada valor de CopyCount en su propia opción, algunos atributos de configuración de dispositivos simplemente no se pueden representar mediante una construcción de característica/opción. Por ejemplo, Imagine un dispositivo que acepta una cadena de texto que se usa para generar una marca de agua virtual en cada página de salida. El conjunto de todas las cadenas de texto posibles no se puede enumerar de forma explícita, pero la cadena de texto se puede describir fácilmente mediante un elemento ParameterDef.

En el documento imprimir palabras clave del esquema se define una serie de construcciones de parámetros de uso frecuente, pero los proveedores de PrintCapabilities son libres para definir otras propias. Sin embargo, estas construcciones de parámetros definidas de forma privada no son portables a otros dispositivos, debido al hecho de que un documento de PrintCapabilities proporcionado por otra parte no define este tipo de parámetro. Tanto si está definido por el esquema como si está definido de forma privada, la instancia de ParameterDef debe estar presente en el documento de PrintCapabilities antes de que los clientes reconocen y utilicen el parámetro. Estos parámetros se conocen como *parámetros designados*.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



