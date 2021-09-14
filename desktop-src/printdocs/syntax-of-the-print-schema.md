---
description: Obtenga información sobre la sintaxis del esquema de impresión, que se expresa en sintaxis XML y se compone de un pequeño número de tipos de elemento.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintaxis del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268332"
---
# <a name="syntax-of-the-print-schema"></a>Sintaxis del esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión se expresa en sintaxis XML. Por lo tanto, se espera que los lectores estén familiarizados con la sintaxis XML y los términos como elemento, etiqueta de elemento, contenido de elemento, atributo y espacio de nombres. El marco de esquema de impresión se compone de un pequeño número de tipos de elementos; Cada tipo de elemento tiene un propósito específico en las tecnologías creadas en el esquema de impresión.

Los tipos de elemento se distinguen por su etiqueta de elemento XML. El marco de esquema de impresión define la estructura general y la organización de las tecnologías dependientes, indicando para cada tipo de elemento qué tipos de elemento se permiten como elementos secundarios.

Muchos tipos de elementos se diferencian de otros del mismo tipo por el atributo name, que desempeña un papel importante en el esquema. El atributo name sirve para identificar instancias de cada tipo de elemento. Las palabras clave de esquema de impresión definen un conjunto de valores para el atributo name para muchos de los tipos de elemento. En la mayoría de los casos, los proveedores pueden asignar sus propios valores al atributo name. Solo necesitan asegurarse de que los valores son QName XML calificados con un espacio de nombres que es único para el proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



