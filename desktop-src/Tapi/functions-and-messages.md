---
description: La función phoneDevSpecific y su mensaje PHONE DEVSPECIFIC asociado permiten a una aplicación acceder a características de teléfono específicas del dispositivo que no están disponibles a través de los servicios de telefonía comunes para \_ teléfonos.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funciones y mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cabdc271548e42b20de695296321f5f5ab0fdbe45a246be2b7ccb1993ee5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660745"
---
# <a name="functions-and-messages"></a>Funciones y mensajes

La [**función phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) y su mensaje [**PHONE \_ DEVSPECIFIC**](phone-devspecific.md) asociado permiten a una aplicación acceder a características de teléfono específicas del dispositivo que no están disponibles a través de los servicios de telefonía comunes para teléfonos. En otras palabras, **phoneDevSpecific** es la función de escape específica del dispositivo que permite extensiones dependientes del proveedor y PHONE DEVSPECIFIC es el mensaje específico del dispositivo que se envía a la \_ aplicación.

El perfil de parámetro de [**la función phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) es genérico, ya que TAPI realiza una interpretación pequeña de los parámetros. En su lugar, el proveedor de servicios define la interpretación de los parámetros y la debe entender una aplicación que los use. TapI simplemente pasa los parámetros desde la aplicación al proveedor de servicios. Normalmente, una aplicación que se basa en extensiones específicas del dispositivo no funcionará con otros proveedores de servicios, pero las aplicaciones escritas en los servicios telefónicos de telefonía comunes funcionarán con el proveedor de servicios extendidos.

 

 



