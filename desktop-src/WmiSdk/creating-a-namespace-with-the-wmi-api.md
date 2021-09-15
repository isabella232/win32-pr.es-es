---
description: Otra manera de crear un espacio de nombres es usar la API de WMI para crear el espacio de nombres mediante programación.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Creación de un espacio de nombres con la API wmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569368"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Creación de un espacio de nombres con la API wmi

Otra manera de crear un espacio de nombres es usar la API de WMI para crear el espacio de nombres mediante programación. La ventaja de crear un espacio de nombres mediante programación es que puede crear el espacio de nombres desde dentro de una aplicación. Sin embargo, el uso de la API wmi es más complejo que usar Managed Object Format (MOF) y no puede compartir fácilmente los espacios de nombres con otros desarrolladores.

En el procedimiento siguiente se describe cómo crear un espacio de nombres mediante la API de WMI.

**Para crear un espacio de nombres mediante la API wmi**

1.  Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar un puntero a un objeto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunta a la clase del sistema [**\_ \_ Namespace.**](--namespace.md)
2.  Defina una instancia de la clase del sistema [**\_ \_ Namespace**](--namespace.md) con una llamada a [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Establezca la **propiedad Name** de la instancia [**\_ \_ namespace**](--namespace.md) con una llamada a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Cree el espacio de nombres con una llamada a [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    El *parámetro pInst* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) debe apuntar a la nueva instancia.

 

 



