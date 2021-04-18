---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Referencia a parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707624"
---
# <a name="referencing-parameters"></a>Referencia a parámetros

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un ejemplo concreto de una opción que incluye un elemento ParameterRef es la opción de tamaño multimedia personalizado. Tenga en cuenta que hace referencia a dos parámetros: PageMediaSizeMediaSizeWidth y PageMediaSizeMediaSizeHeight. Cada instancia de ParameterRef hace referencia a una instancia de ParameterDef que se define en otra parte del documento de PrintCapabilities. Para obtener información sobre el elemento ParameterDef, vea [ParameterDef](parameterdef.md). Para obtener información conceptual acerca de la definición de parámetros, vea [elementos ParameterDef y ParameterInit](parameterdef-and-parameterinit-elements.md).

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

Simplemente no basta con crear una opción parametrizada para asegurarse de que la opción se controlará y procesará correctamente. Los clientes y el proveedor de PrintCapabilities/PrintTicket deben proporcionar compatibilidad adicional para implementar correctamente instancias de opciones con parámetros. Los comportamientos necesarios se describen en las secciones siguientes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



