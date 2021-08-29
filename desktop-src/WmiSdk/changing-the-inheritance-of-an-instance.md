---
description: Puede encontrar una situación en la que una instancia que se creó como elemento secundario de una clase primaria debe cambiar las clases primarias y convertirse en el elemento secundario de una clase primaria diferente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Cambiar la herencia de una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644b05368cdfe6fbe3e05d94704593544fc18e4408d0f64708021fa1e8c8ca37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612595"
---
# <a name="changing-the-inheritance-of-an-instance"></a>Cambiar la herencia de una instancia

Puede encontrar una situación en la que una instancia que se creó como elemento secundario de una clase primaria debe cambiar las clases primarias y convertirse en el elemento secundario de una clase primaria diferente. Por ejemplo, puede tener una clase derivada, **ManualService**, que describe un servicio manual y una clase derivada, **AutoService**, que describe un servicio automático. Ambas clases tienen un gran número de propiedades. No todas las propiedades son idénticas. Para cambiar un servicio de manual a automático, también debe cambiar la instancia que representa el servicio de **ManualService** a **AutoService**. En la versión actual de WMI, no se puede llamar al método [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) con el parámetro *pInst* que apunta a una instancia de **AutoService** y las propiedades clave que describen la **instancia manualService.** Si lo hace, eliminará implícitamente la instancia original **de ManualService.** Básicamente, después de establecer la clase de una instancia, solo puede cambiar la clase primaria de una instancia eliminando la instancia y volviendo a crear la instancia como una instancia de la nueva clase primaria.

En el procedimiento siguiente se describe cómo mover una instancia de una clase a otra.

**Para mover una instancia de una clase a otra**

1.  Elimine la instancia de la clase original.
2.  Cree la instancia en la nueva clase.

    WMI no permite que las aplicaciones muevan una instancia mediante su creación en la nueva clase y, a continuación, actualizándola con la clave de la instancia original.

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

 

 



