---
description: La función phoneDevSpecific y su \_ mensaje DEVSPECIFIC de teléfono asociado permiten a una aplicación tener acceso a características telefónicas específicas del dispositivo que no están disponibles a través de los servicios de telefonía comunes para teléfonos.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funciones y mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001929"
---
# <a name="functions-and-messages"></a>Funciones y mensajes

La función [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) y su mensaje [**\_ DEVSPECIFIC de teléfono**](phone-devspecific.md) asociado permiten a una aplicación tener acceso a características telefónicas específicas del dispositivo que no están disponibles a través de los servicios de telefonía comunes para teléfonos. En otras palabras, **phoneDevSpecific** es la función de escape específica del dispositivo que permite extensiones dependientes del proveedor y teléfono \_ DEVSPECIFIC es el mensaje específico del dispositivo que se envía a la aplicación.

El perfil de parámetro de la función [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) es genérico, ya que la interpretación de los parámetros la realiza TAPI. En su lugar, la interpretación de los parámetros se define mediante el proveedor de servicios y debe ser entendida por una aplicación que los utiliza. Los parámetros se pasan simplemente por TAPI desde la aplicación al proveedor de servicios. Normalmente, una aplicación que se basa en extensiones específicas del dispositivo no funcionará con otros proveedores de servicios, pero las aplicaciones escritas en los servicios del teléfono de telefonía común funcionarán con el proveedor de servicios extendidos.

 

 



