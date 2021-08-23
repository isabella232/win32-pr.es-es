---
description: Monitor de red proporciona una estructura PROPERTYINFO para definir las propiedades de un protocolo y una estructura PROPERTYINST y PROPERTYINSTEX para definir una instancia de una propiedad.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definición de propiedad y estructuras de instancia de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8289c16bf501d36936b1aba6f292787e1b9a41babdb1225d3c0d53885c0ba31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676824"
---
# <a name="property-definition-and-property-instance-structures"></a>Definición de propiedad y estructuras de instancia de propiedad

Monitor de red proporciona una [**estructura PROPERTYINFO**](propertyinfo.md) para definir las propiedades de un protocolo y una [**estructura PROPERTYINST**](propertyinst.md)y [**PROPERTYINSTEX**](propertyinstex.md) para definir una instancia de una propiedad.

![estructuras de supervisión de red](images/property1.png)

El analizador asigna y rellena la estructura [**PROPERTYINFO**](propertyinfo.md) para todas las propiedades que admite un protocolo. El analizador pasa la estructura a Monitor de red donde la estructura se agrega a la base de datos de [*propiedades de protocolo*](p.md). La información de la **estructura PROPERTYINFO** se usa al analizar una instancia de una propiedad y al dar formato a los datos que se muestran en la interfaz Monitor de red usuario.

Monitor de red asigna las estructuras [**PROPERTYINST**](propertyinst.md) y [**PROPERTYINSTEX**](propertyinstex.md) cuando el analizador asocia una definición de propiedad a una instancia de una propiedad.

El procedimiento siguiente identifica los pasos necesarios para adjuntar una definición de propiedad.

**Para adjuntar una definición de propiedad**

1.  Identifique cada propiedad que existe en una instancia del protocolo. Al adjuntar una definición, Monitor de red pasa los datos capturados al analizador. Los datos se pasan en función de una instancia de protocolo.
2.  Determine la ubicación de la propiedad en la instancia de protocolo.
3.  Adjunte una definición de propiedad a la ubicación de la propiedad.

Monitor de red implementa una [**estructura PROPERTYINST**](propertyinst.md) cuando el analizador usa los datos de propiedad tal como existen en la captura. Monitor de red implementa una [**estructura PROPERTYINSTEX**](propertyinstex.md) cuando el analizador debe modificar los datos de propiedad en la captura.

 

 



