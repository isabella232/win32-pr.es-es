---
description: Esta \_ función TSPI lineSetCurrentLocation está obsoleta. TAPI llamó a esta función cuando el usuario (mediante el cuadro de diálogo Propiedades de marcado) o una aplicación (mediante la función lineSetCurrentLocation) cambió la ubicación de traducción de direcciones.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814363"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

Esta \_ función TSPI lineSetCurrentLocation está obsoleta. TAPI llamó a esta función cuando el usuario (mediante el cuadro de diálogo **propiedades de marcado** ) o una aplicación (mediante la función [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) cambió la ubicación de traducción de direcciones.

Actualmente, un cambio en la ubicación de traducción da como resultado un \_ mensaje line DEVSTATE con *dwParam1* establecido en LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
