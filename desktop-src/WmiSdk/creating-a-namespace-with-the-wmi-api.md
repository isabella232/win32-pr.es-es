---
description: Otra forma de crear un espacio de nombres es usar la API de WMI para crear el espacio de nombres mediante programación.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Crear un espacio de nombres con la API de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715840"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Crear un espacio de nombres con la API de WMI

Otra forma de crear un espacio de nombres es usar la API de WMI para crear el espacio de nombres mediante programación. La ventaja de crear un espacio de nombres mediante programación es que se puede crear el espacio de nombres desde dentro de una aplicación. Sin embargo, el uso de la API de WMI es más complejo que el uso de código de Managed Object Format (MOF) y no se pueden compartir fácilmente los espacios de nombres con otros desarrolladores.

En el procedimiento siguiente se describe cómo crear un espacio de nombres mediante la API de WMI.

**Para crear un espacio de nombres mediante la API de WMI**

1.  Use [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar un puntero a un objeto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunte a la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) .
2.  Defina una instancia de la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) con una llamada a [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Establezca la propiedad **Name** de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) con una llamada a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Cree el espacio de nombres con una llamada a [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    El parámetro *PIN* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) debe apuntar a la nueva instancia.

 

 



