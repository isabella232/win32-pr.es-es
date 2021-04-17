---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintaxis del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698022"
---
# <a name="syntax-of-the-print-schema"></a>Sintaxis del esquema de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión se expresa en sintaxis XML. Por tanto, se espera que los lectores estén familiarizados con la sintaxis XML y con términos como elemento, etiqueta de elemento, contenido de elemento, atributo y espacio de nombres. El marco de trabajo del esquema de impresión se compone de un número pequeño de tipos de elemento. cada tipo de elemento sirve a un propósito específico en las tecnologías basadas en el esquema de impresión.

Los tipos de elemento se distinguen por su etiqueta de elemento XML. El marco de trabajo del esquema de impresión define la estructura global y la organización de las tecnologías dependientes, indicando para cada tipo de elemento qué tipos de elemento se permiten como elementos secundarios.

Muchos tipos de elementos se diferencian de otros del mismo tipo por el atributo name, que desempeña un rol significativo en el esquema. El atributo name sirve para identificar las instancias de cada tipo de elemento. Las palabras clave de esquema de impresión definen un conjunto de valores para el atributo de nombre para muchos de los tipos de elemento. En la mayoría de los casos, los proveedores pueden asignar sus propios valores al atributo de nombre. Solo necesitan asegurarse de que los valores sean QNames XML calificados con un espacio de nombres que sea único para el proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



