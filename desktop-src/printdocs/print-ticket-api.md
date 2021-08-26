---
description: Print Ticket API permite a las aplicaciones administrar y convertir vales de impresión.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API de impresión de vales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91cc976addba630bae3f250d244442ba1dd3b61f741575fe21cb250bab4a2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947804"
---
# <a name="print-ticket-api"></a>API de impresión de vales

Print Ticket API permite a las aplicaciones administrar y convertir vales de impresión.

Un vale de impresión es un componente de documento XPS que contiene la configuración de impresora preferida para una página de un documento, para un documento completo o para un trabajo de impresión que contiene uno o varios documentos. Tenga en cuenta que los vales de impresión solo se encuentran en documentos XPS.

Para que la impresora pueda usar el vale de impresión, el vale de impresión debe validarse con las características de la impresora, que se definen en las capacidades de impresión de la impresora. La aplicación realiza esa validación mediante una llamada a print ticket API.

PrintTicket e PrintCapabilities se describen mediante el uso de elementos del esquema de impresión, que se define mediante la especificación [de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Este tema contiene información sobre los siguientes elementos de API:

-   [Funciones de API de vales de impresión](print-ticket-api-functions.md)
-   [Enumeraciones de API de vales de impresión](print-ticket-api-enumerations.md)

En el diagrama siguiente se muestra la relación de Print Ticket API con las otras API de impresión que puede Windows aplicación nativa.

![diagrama que muestra la relación de la API de vale de impresión con las otras API de impresión que puede usar una aplicación nativa de Windows](images/print-apis-pt.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XPS Print API](xps-printing.md)
</dt> <dt>

[Print Spooler API](print-spooler-api.md)
</dt> <dt>

[API de impresión de GDI](gdi-printing.md)
</dt> <dt>

[Especificación del esquema de impresión](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



