---
description: Los consumidores de documentos PrintCapabilities tienen ciertas obligaciones que deben cumplir para poder usar un documento PrintCapabilities.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilidades de los consumidores del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec123509515de32b88c7352dcf0fc2c2b54504ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570545"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilidades de los consumidores del documento PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los consumidores de documentos PrintCapabilities tienen ciertas obligaciones que deben cumplir para poder usar un documento PrintCapabilities. Los siguientes requisitos se aplican a los clientes de un documento PrintCapabilities.

-   No deben rechazar ni no procesar ninguna propiedad PrintCapabilities válida sintácticamente; es decir, cualquier documento PrintCapabilities que se ajuste al esquema PrintCapabilities.

-   Deben ser capaces de evitar la presencia inesperada o ausencia de contenido definido de forma privada. Esto incluye contenido definido de forma privada que aparece dentro de instancias de elementos definidos por el esquema de impresión.

-   Deben ser capaces de evitar contenido opcional del esquema de impresión que no esté presente.

-   Deben tener en cuenta cuándo solicitar un nuevo documento.

    -   Los valores de las instancias de propiedad dependen de la configuración (por lo tanto, dependientes de la instantánea). Debe actualizar la instantánea cuando acceda a una instancia de Propiedad.

    -   Las instancias Feature, Option y ScoredProperty que se van a copiar en printTicket son estáticas por definición. Es decir, no dependen (ni deben ser) de la configuración del dispositivo. Si accede a cualquier instancia de estos tipos, no es necesario obtener un nuevo documento PrintCapabilities cuando cambie la configuración.

-   Los consumidores de PrintCapabilities que son clientes de interfaz de usuario (UI) deben poder usar la información de un documento PrintCapabilities para construir una interfaz de usuario y construir un PrintTicket válido a partir de las selecciones de usuario. Esto incluye saber qué instancias de ParameterInit deben especificarse y validar las instancias especificadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



