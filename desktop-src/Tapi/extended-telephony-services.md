---
description: La API contiene un mecanismo que permite a los proveedores de proveedores de servicios extender la API de telefonía mediante extensiones específicas del dispositivo.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Servicios de telefonía extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a319f59f51643fb5bf13ec95800d40ffa6d8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677806"
---
# <a name="extended-telephony-services"></a>Servicios de telefonía extendidos

La API contiene un mecanismo que permite a los proveedores de proveedores de servicios extender la API de telefonía mediante extensiones específicas del dispositivo. Los servicios de telefonía extendidos (o los servicios específicos del dispositivo) incluyen todas las extensiones de la API definidas por un proveedor de servicios determinado. Dado que la API define solo el mecanismo de extensión, el proveedor de servicios debe especificar por completo la definición del comportamiento del servicio Extended-Telephony.

## <a name="tapi-2x-extended-telephony"></a>Telefonía extendida TAPI 2. x

El mecanismo de extensión permite a los proveedores de proveedores de servicios definir valores nuevos para algunos tipos de enumeración y marcadores de bits, y agregar miembros a la mayoría de las estructuras de datos. La interpretación de las extensiones se ha codificado fuera del identificador de la extensión del proveedor de servicios, un identificador para la especificación del conjunto de extensiones admitidas, que puede cruzar varios fabricantes. En la API se proporcionan funciones y mensajes especiales, como [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) y [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) , para permitir que una aplicación se comunique directamente con un proveedor de servicios. El proveedor de servicios también define los parámetros de cada función.

No es necesario que los proveedores se registren para tener asignados identificadores de extensión. En su lugar, se proporciona una utilidad llamada EXTIDGEN (Extidgen.exe) en el kit de desarrollo de software (SDK) de la plataforma que permite la generación local de identificadores de extensión. Este identificador único se compone de una dirección de adaptador Ethernet, un número aleatorio y la hora del día. Un identificador se asigna a un conjunto de extensiones (antes de la distribución), no a cada instancia individual de una implementación de esas extensiones.

 

 
