---
description: Los servicios de línea extendidos (o servicios de línea específicos del dispositivo) incluyen todas las extensiones definidas por el proveedor de servicios a la API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Funciones de línea extendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394ad011a5752a45f82de4934a3f87c9f1590870b245fdc113f57badb4298290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003663"
---
# <a name="extended-line-functions"></a>Funciones de línea extendidas

Los servicios de línea extendidos (o servicios de línea específicos del dispositivo) incluyen todas las extensiones definidas por el proveedor de servicios a la API. La API define un mecanismo que permite a los proveedores de proveedores de servicios ampliar TAPI mediante extensiones específicas del dispositivo. La API solo define el mecanismo de extensión y, al hacerlo, proporciona acceso a extensiones específicas del dispositivo, pero la API no define su comportamiento. El proveedor de servicios define completamente el comportamiento.

TAPI consta de definiciones de constantes escalares y de marca de bits, estructuras de datos, funciones y mensajes. Se definen procedimientos que permiten a un proveedor ampliar la mayoría de estos procedimientos como se muestra a continuación.

Para las constantes de datos escalares extensibles, un proveedor de servicios puede definir nuevos valores en un intervalo especificado. Como la mayoría de las constantes de datos son **DWORD,** normalmente el intervalo 0x00000000 a 0x7FFFFFFF está reservado para extensiones futuras comunes, mientras que 0x80000000 a 0xFFFFFFFF están disponibles para extensiones específicas del proveedor. La suposición es que un proveedor definiría valores que son extensiones naturales de los tipos de datos definidos por la API.

Para las constantes de datos extensibles de marca de bits, un proveedor de servicios puede definir nuevos valores para los bits especificados. Como la mayoría de las constantes de marca de bits son **DWORD,** normalmente un número específico de los bits inferiores se reserva para las extensiones comunes, mientras que los bits superiores restantes están disponibles para las extensiones específicas del proveedor. Las marcas de bits comunes se asignan de cero a arriba; Las extensiones específicas del proveedor deben asignarse desde el bit 31 hacia abajo. Esto proporciona la máxima flexibilidad a la hora de asignar posiciones de bits a extensiones comunes frente a extensiones específicas del proveedor. Se espera que un proveedor defina nuevos valores que sean extensiones naturales de las marcas de bits definidas por la API.

Las estructuras de datos extensibles tienen un campo de tamaño variable que está reservado para uso específico del dispositivo. Al tener un tamaño variable, el proveedor de servicios decide la cantidad de información y la interpretación. Se espera que un proveedor que defina un campo específico del dispositivo realice estas extensiones naturales de la estructura de datos original definida por la API.

Dos funciones, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) y [**lineDevSpecificFeature,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)y dos mensajes relacionados, [**LINE \_ DEVSPECIFIC**](line-devspecific.md) y [**LINE \_ DEVSPECIFICFEATURE,**](line-devspecificfeature.md)proporcionan un mecanismo de extensión específico del proveedor. La **función lineDevSpecific** y el mensaje LINE DEVSPECIFIC asociado permiten a una aplicación acceder a características de línea, dirección o llamada específicas del dispositivo que no están disponibles con los servicios de telefonía básica o \_ complementaria. El perfil de parámetro de la **función lineDevSpecific** es genérico, ya que la API realiza poca interpretación de los parámetros. El proveedor de servicios define la interpretación de los parámetros y la debe entender una aplicación que los use. Los parámetros simplemente se pasan a través de TAPI desde la aplicación al proveedor de servicios. Por lo general, una aplicación que se basa en extensiones específicas del dispositivo no funcionará con otros proveedores de servicios. sin embargo, las aplicaciones escritas en los servicios de telefonía básica y complementaria funcionarán con el proveedor de servicios extendidos.

Para mayor comodidad, también se proporciona una función de escape más especializada. Es similar a [**lineDevSpecific,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)pero coloca la interpretación en algunos de los parámetros. Esta función más especializada es [**lineDevSpecificFeature,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)una función de escape específica del dispositivo que permite enviar características de modificador al conmutador. El mensaje [**LINE \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) es el mensaje específico del dispositivo que se envía a la aplicación como indicación de las características enviadas al conmutador. Esta función y su mensaje asociado permiten a una aplicación emular las pulsaciones de botón en el teléfono de características de la línea. Como los teléfonos de características y los significados de sus botones son específicos del proveedor, la invocación de características mediante [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) también es específica del proveedor.

Como se mencionó anteriormente, no hay ningún registro central para los identificadores de fabricante. En su lugar, se hace disponible un generador de identificadores únicos (EXTIDGEN).

 

 



