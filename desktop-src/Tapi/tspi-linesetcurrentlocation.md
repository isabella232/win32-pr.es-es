---
description: Esta función lineSetCurrentLocation de TSPI \_ está obsoleta. TAPI llamó a esta función cuando el usuario (mediante el cuadro de diálogo Propiedades de marcado) o una aplicación (mediante la función lineSetCurrentLocation) cambiaron la ubicación de traducción de direcciones.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa78427bc4892fd0460b60bcb90f5fef43a38f002368c7ca7251cb1ce611c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012125"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

Esta función lineSetCurrentLocation de TSPI \_ está obsoleta. TAPI llamó a esta función  cuando el usuario (mediante el cuadro de diálogo Propiedades de marcado) o una aplicación (mediante la función [**lineSetCurrentLocation)**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) cambiaron la ubicación de traducción de direcciones.

Actualmente, un cambio en la ubicación de traducción da como resultado un mensaje LINE \_ DEVSTATE con *dwParam1* establecido en LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
