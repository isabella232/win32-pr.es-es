---
description: Un proveedor de propiedades usa los métodos IWbemPropertyProvider como interfaz principal para WMI. Con IWbemPropertyProvider, puede implementar el código para recuperar y modificar las propiedades de la clase y de la instancia.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716556"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a>Implementar la interfaz principal para un proveedor de propiedades

Un proveedor de propiedades usa los métodos [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) como interfaz principal para WMI. Con **IWbemPropertyProvider**, puede implementar el código para recuperar y modificar las propiedades de la clase y de la instancia.

En la tabla siguiente se enumeran los métodos de [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) que se pueden implementar para un proveedor de propiedades.



| Método                                                   | Característica      |
|----------------------------------------------------------|--------------|
| [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | Recuperación    |
| [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | Modificación |



 

> [!Note]  
> Debe implementar un proveedor de propiedades como un proveedor en proceso. WMI inicializará los proveedores de propiedades escritos como servicios o archivos ejecutables, pero nunca llamará a sus métodos [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) y [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .

 

Si decide no admitir uno de estos métodos, el proveedor puede proporcionar una implementación de código auxiliar que devuelva el **proveedor de WBEM \_ E \_ \_ no \_ compatible**.

Un proveedor de propiedades identifica una clase o instancia administrada mediante un conjunto de tres calificadores: **PropertyContext**, **InstanceContext** y **ClassContext**. WMI pasará las constantes de cadena que describen estos tres calificadores al proveedor de propiedades.

El proveedor de propiedades debe estar preparado para controlar los siguientes tipos de calificadores de contexto:

-   El calificador **InstanceContext** se adjunta a una instancia de y contiene información que se aplica a todas las propiedades de la instancia.
-   El calificador **ClassContext** se adjunta a una clase y contiene información que se aplica a todas las instancias de la clase. Por ejemplo, en una clase que se usa para almacenar los datos suministrados por el proveedor del registro, **ClassContext** puede ser la ruta de acceso a la clave del registro que contiene las propiedades que se van a informar.
-   El calificador **PropertyContext** especifica la información específica del contexto que pertenece a la propiedad. Por ejemplo, en una clase que se usa para almacenar los datos suministrados por el proveedor del registro, **PropertyContext** especifica el nombre del valor del registro que la propiedad va a almacenar.

Estos calificadores pueden funcionar juntos. Puede designar un valor **InstanceContext** y **PropertyContext** para indicar al proveedor cómo tratar determinados tipos de instancias. Por ejemplo, puede marcar las instancias que el proveedor reconocerá como legibles pero con una sola propiedad que se puede escribir.

El calificador más común que se usa es **PropertyContext**. Por lo tanto, WMI proporciona el calificador **DynProps** como un acceso directo. WMI considera que cada propiedad de una instancia marcada con **DynProps** también tiene los calificadores **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **PropertyContext** .

 

 



