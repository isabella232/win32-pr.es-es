---
description: Los servicios de telefonía adicionales son la colección de todos los servicios definidos por la API que no son los que se incluyen en el subconjunto de telefonía básico.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Servicios de telefonía adicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909609"
---
# <a name="supplementary-telephony-services"></a>Servicios de telefonía adicionales

Los servicios de telefonía adicionales son la colección de todos los servicios definidos por la API que no son los que se incluyen en el subconjunto de telefonía básico. Incluye todas las características complementarias que se encuentran en las PBX modernas, como la retención, la transferencia, la Conferencia, el parque, etc. Todas las características complementarias se consideran opcionales; es decir, el proveedor de servicios decide qué servicios realiza o no proporciona.

Una aplicación puede consultar un dispositivo de línea o de teléfono para obtener el conjunto de servicios complementarios que proporciona mediante funciones como [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) o [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps). Un único servicio complementario puede constar de varias llamadas de función y mensajes. La API de telefonía, y no el desarrollador de proveedores de servicios, define el comportamiento de cada una de estas características complementarias. Un proveedor de servicios debe proporcionar un servicio de telefonía suplementario solo si puede implementar el significado exacto tal y como se define en la API. Si no es así, la característica debe proporcionarse como un servicio de telefonía extendido.

Como se mencionó en servicios de telefonía básicos, los servicios de dispositivos telefónicos se consideran opcionales. Por lo tanto, todos los servicios de dispositivo telefónico forman parte de la telefonía complementaria. Para obtener una lista de las funciones de telefonía complementaria, consulte [referencia de funciones rápidas de TAPI](./tapi-quick-function-reference.md).

 

 
