---
description: En esta introducción a la funcionalidad PrintTicket se describe el formato para expresar la información de configuración del dispositivo y el uso de un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Información general de la funcionalidad PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263084"
---
# <a name="overview-of-printticket-functionality"></a>Información general de la funcionalidad PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintTicket usa un formato basado en XML para expresar la información de configuración del dispositivo mediante las construcciones feature/option y de parámetros de Print Schema Framework. Esto incluye todos los tipos de elementos estándar, así como las funcionalidades de extensibilidad de Print Schema Framework. Se supone que printticket es una descripción independiente de cómo se va a procesar una sola página. Los pasos necesarios para extraer y construir este tipo de PrintTicket a partir de un formato de documento determinado no se tratan aquí.

Un PrintTicket se puede usar para obtener un documento PrintCapabilities que describa las características del dispositivo para una configuración determinada. Como alternativa, printticket se puede enviar con un conjunto de instrucciones de representación para generar una página de salida representado y procesado según la configuración especificada en PrintTicket.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



