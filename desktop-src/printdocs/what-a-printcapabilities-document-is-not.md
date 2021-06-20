---
description: Obtenga información sobre algunas de las funcionalidades y la información que el documento PrintCapabilities no pretende proporcionar.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Qué no es un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409898"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Qué no es un documento PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Merece la pena enumerar parte de la funcionalidad y la información que el documento PrintCapabilities no pretende proporcionar.

Un documento PrintCapabilities:

-   No representa datos multivalor (dependientes de la configuración).

    Cada documento PrintCapabilities se construye para una configuración específica. Ninguna propiedad o ScoredProperty en el documento puede tener un valor que dependa de la configuración determinada. En la versión inicial del esquema, el proveedor PrintCapabilities debe procesar la entrada PrintTicket y crear un documento PrintCapabilities que contenga los valores property adecuados para la configuración especificada en PrintTicket.

-   No contiene información de restricción.

    El documento PrintCapabilities no indica qué configuraciones se permiten y cuáles no. En la versión inicial del esquema, el proveedor PrintCapabilities debe almacenar toda la información necesaria para validar las configuraciones, proporcionar un método que valide la entrada PrintTicket y devolver un PrintTicket corregido en caso de que el PrintTicket especificado infrinja una o varias restricciones.

-   No contiene información dinámica del dispositivo.

    Hay demasiada sobrecarga implicada en la construcción del documento PrintCapabilities para que se utilice para contener información de estado que cambia rápidamente, como los niveles de entrada de lápiz, el papel restante en cada bandeja o el estado de la entrada de papel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



