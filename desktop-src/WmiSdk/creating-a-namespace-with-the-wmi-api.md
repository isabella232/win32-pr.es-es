---
description: Otra manera de crear un espacio de nombres es usar la API wmi para crear el espacio de nombres mediante programación.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Creación de un espacio de nombres con la API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192bb38b60c3d0ddefb8cc1e5cb7b5f78cb0f5ba7937d39784729e0f61f70b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612545"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Creación de un espacio de nombres con la API WMI

Otra manera de crear un espacio de nombres es usar la API wmi para crear el espacio de nombres mediante programación. La ventaja de crear un espacio de nombres mediante programación es que puede crear el espacio de nombres desde dentro de una aplicación. Sin embargo, el uso de la API WMI es más complejo que usar Managed Object Format (MOF) y no puede compartir fácilmente los espacios de nombres con otros desarrolladores.

En el procedimiento siguiente se describe cómo crear un espacio de nombres mediante la API wmi.

**Para crear un espacio de nombres mediante la API WMI**

1.  Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar un puntero a un [**objeto IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que apunta a la clase del sistema [**\_ \_ Namespace.**](--namespace.md)
2.  Defina una instancia de la clase del sistema [**\_ \_ Namespace**](--namespace.md) con una llamada a [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Establezca la **propiedad Name** de la instancia [**\_ \_ de Namespace**](--namespace.md) con una llamada a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Cree el espacio de nombres con una llamada a [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    El *parámetro pInst* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) debe apuntar a la nueva instancia.

 

 



