---
description: Obtenga información sobre cómo hacer referencia a parámetros y el elemento ParameterDef. Un ejemplo de una opción que incluye un elemento ParameterRef es el tamaño de medio personalizado Option.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Referencia a parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359695"
---
# <a name="referencing-parameters"></a>Referencia a parámetros

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un ejemplo concreto de una opción que incluye un elemento ParameterRef es la opción de tamaño de medio personalizado. Tenga en cuenta que hace referencia a dos parámetros: PageMediaSizeMediaSizeWidth y PageMediaSizeMediaSizeHeight. Cada instancia de ParameterRef hace referencia a una instancia de ParameterDef que se define en otra parte del documento PrintCapabilities. Para obtener información sobre el elemento ParameterDef, vea [ParameterDef](parameterdef.md). Para obtener información conceptual sobre cómo definir parámetros, vea [ParameterDef y ParameterInit Elements](parameterdef-and-parameterinit-elements.md).

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

La simple creación de una opción parametrizada no es suficiente para asegurarse de que la opción se controlará y procesará correctamente. El proveedor PrintCapabilities/PrintTicket y los clientes deben proporcionar compatibilidad adicional para implementar correctamente instancias option parametrizadas. Los comportamientos necesarios se describen en las secciones siguientes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



