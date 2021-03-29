---
description: Los servicios de línea ampliada (o los servicios de línea específicos del dispositivo) incluyen todas las extensiones definidas por el proveedor de servicios a la API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Funciones de línea extendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3531a63357276e6b2ea37365b5d5078d5c1de324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541779"
---
# <a name="extended-line-functions"></a>Funciones de línea extendida

Los servicios de línea ampliada (o los servicios de línea específicos del dispositivo) incluyen todas las extensiones definidas por el proveedor de servicios a la API. La API define un mecanismo que permite a los proveedores de proveedores de servicios ampliar TAPI con extensiones específicas del dispositivo. La API solo define el mecanismo de extensión y, al hacerlo, proporciona acceso a extensiones específicas del dispositivo, pero la API no define su comportamiento. El proveedor de servicios define el comportamiento por completo.

TAPI consta de definiciones de constantes, estructuras de datos, funciones y mensajes de marcas de bits y escalares. Se definen procedimientos que permiten a un proveedor extender la mayoría de ellos de la manera siguiente.

En el caso de las constantes de datos escalares extensibles, un proveedor de proveedores de servicios puede definir nuevos valores en un intervalo especificado. Como la mayoría de las constantes de datos son **DWORD** s, normalmente el intervalo de 0X00000000 a 0x7FFFFFFF está reservado para extensiones futuras comunes, mientras que 0X80000000 a 0xFFFFFFFF están disponibles para las extensiones específicas del proveedor. La suposición es que un proveedor definiría valores que son extensiones naturales de los tipos de datos definidos por la API.

En el caso de las constantes de datos de marca de bits extensible, un proveedor de proveedor de servicios puede definir nuevos valores para los bits especificados. Como la mayoría de las constantes de marcador de bits son **DWORD** s, normalmente un número específico de los bits inferiores se reserva para las extensiones comunes mientras que los bits superiores restantes están disponibles para las extensiones específicas del proveedor. Las marcas de bits comunes se asignan desde el bit cero hacia arriba; las extensiones específicas del proveedor se deben asignar del bit 31 a la baja. Esto proporciona la máxima flexibilidad para asignar posiciones de bits a extensiones comunes frente a extensiones específicas del proveedor. Se espera que un proveedor defina nuevos valores que son extensiones naturales de las marcas de bits definidas por la API.

Las estructuras de datos extensibles tienen un campo de tamaño variable que se reserva para uso específico del dispositivo. Con el tamaño de variable, el proveedor de servicios decide la cantidad de información y la interpretación. Se espera que un proveedor que define un campo específico del dispositivo realice estas extensiones naturales de la estructura de datos original definida por la API.

Dos funciones, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) y [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), y dos mensajes relacionados, [**\_ DEVSPECIFIC de línea**](line-devspecific.md) y [**\_ DEVSPECIFICFEATURE de línea**](line-devspecificfeature.md), proporcionan un mecanismo de extensión específico del proveedor. La función **lineDevSpecific** y el mensaje DEVSPECIFIC de línea asociada \_ permiten a una aplicación tener acceso a las características de línea, dirección o llamada específicas del dispositivo que no están disponibles con los servicios de telefonía básicos o adicionales. El perfil de parámetro de la función **lineDevSpecific** es genérico, ya que la API realiza una ligera interpretación de los parámetros. La interpretación de los parámetros se define mediante el proveedor de servicios y debe ser entendida por una aplicación que los utiliza. Los parámetros simplemente se pasan a través de TAPI desde la aplicación al proveedor de servicios. Por lo general, una aplicación que se basa en extensiones específicas del dispositivo no funcionará con otros proveedores de servicios; sin embargo, las aplicaciones escritas en los servicios de telefonía básico y complementario funcionarán con el proveedor de servicios extendidos.

Para mayor comodidad, también se proporciona una función de escape más especializada. Es similar a [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific), pero coloca la interpretación en algunos de los parámetros. Esta función más especializada es [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), una función de escape específica del dispositivo para permitir el envío de características de conmutador al conmutador. La línea de mensaje [**\_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) es el mensaje específico del dispositivo que se envía a la aplicación como una indicación de las características enviadas al conmutador. Esta función y su mensaje asociado permiten a una aplicación emular las pulsaciones de botón en el teléfono de características de la línea. Como los teléfonos de características y los significados de sus botones son específicos del proveedor, la invocación de características con [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) también es específica del proveedor.

Como se mencionó anteriormente, no hay ningún registro central para los identificadores de fabricante. En su lugar, se pone a disposición un generador de identificador único (EXTIDGEN).

 

 



