---
description: Print ticket API proporciona permite a las aplicaciones administrar y convertir vales de impresión.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: Print ticket API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083596"
---
# <a name="print-ticket-api"></a>Print ticket API

Print ticket API proporciona permite a las aplicaciones administrar y convertir vales de impresión.

Una solicitud de impresión es un componente de documento XPS que contiene la configuración de impresora preferida para una página de un documento o para un documento completo, o para un trabajo de impresión que contiene uno o varios documentos. Tenga en cuenta que los vales de impresión solo se encuentran en los documentos XPS.

Para que la impresora pueda usar el vale de impresión, la solicitud de impresión debe validarse con las características de la impresora, que se definen en las capacidades de impresión de la impresora. La aplicación realiza esa validación mediante una llamada a la API Print ticket.

El PrintTicket y PrintCapabilities se describen mediante el uso de elementos del esquema de impresión, que se define mediante la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Este tema contiene información sobre los siguientes elementos de la API:

-   [Funciones de la API Print ticket](print-ticket-api-functions.md)
-   [Print ticket API (enumeraciones)](print-ticket-api-enumerations.md)

En el diagrama siguiente se muestra la relación de la API de la solicitud de impresión con las otras API de impresión que puede usar una aplicación Windows nativa.

![un diagrama que muestra la relación de la API de la solicitud de impresión con las otras API de impresión que puede usar una aplicación Windows nativa](images/print-apis-pt.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de impresión XPS](xps-printing.md)
</dt> <dt>

[API del administrador de trabajos de impresión](print-spooler-api.md)
</dt> <dt>

[API de impresión GDI](gdi-printing.md)
</dt> <dt>

[Especificación del esquema de impresión](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



