---
description: Normalmente, el acceso directo es adecuado para llamar a un método de proveedor WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construir objetos Parameters y analizar objetos Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002435"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a>Construir objetos Parameters y analizar objetos Parameters

Normalmente, el acceso directo es adecuado para llamar a un [*método de proveedor*](gloss-p.md)WMI. El acceso directo significa ejecutar un método usando la sintaxis *Object. Method* . Sin embargo, en algunos casos, no se puede usar el acceso directo. Además, llamar a un método de proveedor de forma asincrónica desde un script requiere un tipo de llamada [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

El orden de los parámetros de entrada y salida del método se define en el esquema de Managed Object Format (MOF) del método. WMI no impide que se cambie el orden de los parámetros cuando [MOFCOMP](mofcomp.md)vuelve a compilar la clase. Mediante el uso de un objeto [**Parameters**](swbemmethod-inparameters.md) , puede evitar problemas derivados del esquema modificado porque los parámetros de entrada se identifican por su nombre. El parámetro correcto puede verse examinando el calificador de **identificador** de cada parámetro de entrada. El primer parámetro tiene un valor de **identificador** de 0 (cero).

[**Los métodos SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)y [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) proporcionan una manera alternativa de ejecutar un método de proveedor en los casos en los que no es posible ejecutar un método directamente. Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

Para obtener más información sobre los parámetros, vea [construir objetos Parameters](constructing-inparameters-objects.md) y [analizar objetos Parameters](parsing-outparameters-objects.md).

 

 



