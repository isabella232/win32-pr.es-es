---
description: Monitor de red proporciona una estructura PROPERTYINFO para definir las propiedades de un protocolo, y una estructura PROPERTYINST y PROPERTYINSTEX para definir una instancia de una propiedad.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definición de propiedad y estructuras de instancia de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813309"
---
# <a name="property-definition-and-property-instance-structures"></a>Definición de propiedad y estructuras de instancia de propiedad

Monitor de red proporciona una estructura [**PROPERTYINFO**](propertyinfo.md) para definir las propiedades de un protocolo, y una estructura [**PROPERTYINST**](propertyinst.md)y [**PROPERTYINSTEX**](propertyinstex.md) para definir una instancia de una propiedad.

![estructuras de monitor de red](images/property1.png)

El analizador asigna y rellena la estructura [**PROPERTYINFO**](propertyinfo.md) para todas las propiedades que admite un protocolo. El analizador pasa la estructura a Monitor de red donde se agrega la estructura a la [*base de datos de propiedades*](p.md)de protocolo. La información de la estructura **PROPERTYINFO** se utiliza al analizar una instancia de una propiedad y al dar formato a los datos que se muestran en la interfaz de usuario de monitor de red.

Monitor de red asigna las estructuras [**PROPERTYINST**](propertyinst.md) y [**PROPERTYINSTEX**](propertyinstex.md) cuando el analizador adjunta una definición de propiedad a una instancia de una propiedad.

En el procedimiento siguiente se identifican los pasos necesarios para adjuntar una definición de propiedad.

**Para adjuntar una definición de propiedad**

1.  Identifique cada propiedad que exista en una instancia del protocolo. Al adjuntar una definición, Monitor de red pasa los datos capturados al analizador. Los datos se pasan en función de una instancia del protocolo.
2.  Determine la ubicación de la propiedad en la instancia del protocolo.
3.  Adjunte una definición de propiedad a la ubicación de la propiedad.

Monitor de red implementa una estructura [**PROPERTYINST**](propertyinst.md) cuando el analizador utiliza los datos de propiedad tal como existen en la captura. Monitor de red implementa una estructura [**PROPERTYINSTEX**](propertyinstex.md) cuando el analizador debe modificar los datos de la propiedad en la captura.

 

 



