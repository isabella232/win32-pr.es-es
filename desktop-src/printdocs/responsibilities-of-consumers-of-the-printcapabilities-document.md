---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades de los consumidores del documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717417"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilidades de los consumidores del documento de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los consumidores de documentos de PrintCapabilities tienen ciertas obligaciones que deben mantener antes de poder usar un documento de PrintCapabilities. Los siguientes requisitos se aplican a los clientes de un documento de PrintCapabilities.

-   No deben rechazar o no procesar ninguna PrintCapabilities válida sintácticamente. es decir, cualquier documento de PrintCapabilities que se ajuste al esquema de PrintCapabilities.

-   Deben ser capaces de solucionar la presencia inesperada o la ausencia de contenido definido de forma privada. Esto incluye contenido definido de forma privada que aparece dentro de las instancias de los elementos definidos por el esquema de impresión.

-   Deben ser capaces de solucionar el contenido opcional del esquema de impresión que falta.

-   Deben tener en cuenta cuándo solicitar un nuevo documento.

    -   Los valores de las instancias de propiedades dependen de la configuración (por tanto, dependen de la instantánea). Debe actualizar la instantánea cuando tenga acceso a una instancia de propiedad.

    -   Las instancias de Feature, Option y ScoredProperty que se van a copiar en un PrintTicket son por definición static. Es decir, no son (y no deben ser) en función de la configuración del dispositivo. Si obtiene acceso a cualquier instancia de estos tipos, no es necesario obtener un nuevo documento de PrintCapabilities cuando cambia la configuración.

-   Los consumidores de PrintCapabilities que son clientes de interfaz de usuario (IU) deben poder usar la información de un documento de PrintCapabilities para construir una interfaz de usuario y para construir un PrintTicket válido a partir de las selecciones de usuario. Esto incluye saber qué instancias de ParameterInit se deben especificar y validar las instancias especificadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



