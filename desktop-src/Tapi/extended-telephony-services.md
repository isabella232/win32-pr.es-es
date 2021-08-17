---
description: La API contiene un mecanismo que permite a los proveedores de servicios ampliar la API de telefonía mediante extensiones específicas del dispositivo.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Servicios de telefonía extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403f57904138b3797069222875086b0a4990b8e625f701f380120d65c235784e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140708"
---
# <a name="extended-telephony-services"></a>Servicios de telefonía extendidos

La API contiene un mecanismo que permite a los proveedores de servicios ampliar la API de telefonía mediante extensiones específicas del dispositivo. Los servicios de telefonía extendida (o servicios específicos del dispositivo) incluyen todas las extensiones de la API definidas por un proveedor de servicios determinado. Dado que la API define solo el mecanismo de extensión, el proveedor de servicios debe especificar completamente la definición del Extended-Telephony comportamiento del servicio.

## <a name="tapi-2x-extended-telephony"></a>Telefonía extendida tapi 2.x

El mecanismo de extensión permite a los proveedores de servicios definir nuevos valores para algunos tipos de enumeración y marcas de bits y agregar miembros a la mayoría de las estructuras de datos. La interpretación de las extensiones se incluye en el identificador de extensión del proveedor de servicios, un identificador para la especificación del conjunto de extensiones admitidas, que puede cruzar varios fabricantes. En la API se proporcionan funciones y mensajes especiales, como [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) y [**phoneDevSpecific,**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) para permitir que una aplicación se comunique directamente con un proveedor de servicios. El proveedor de servicios también define los parámetros para cada función.

No es necesario que los proveedores se registren para que se les asignen identificadores de extensión. En su lugar, se proporciona una utilidad denominada EXTIDGEN (Extidgen.exe) dentro del Kit de desarrollo de software (SDK) de plataforma que permite la generación local de identificadores de extensión. Este identificador único se compone de una dirección del adaptador Ethernet, un número aleatorio y la hora del día. Un identificador se asigna a un conjunto de extensiones (antes de la distribución), no a cada instancia individual de una implementación de esas extensiones.

 

 
