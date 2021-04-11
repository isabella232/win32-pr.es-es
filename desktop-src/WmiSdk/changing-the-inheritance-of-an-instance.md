---
description: Es posible que encuentre una situación en la que una instancia creada como elemento secundario de una clase primaria debe cambiar las clases primarias y convertirse en el elemento secundario de una clase primaria diferente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Cambiar la herencia de una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910294"
---
# <a name="changing-the-inheritance-of-an-instance"></a>Cambiar la herencia de una instancia

Es posible que encuentre una situación en la que una instancia creada como elemento secundario de una clase primaria debe cambiar las clases primarias y convertirse en el elemento secundario de una clase primaria diferente. Por ejemplo, puede tener una clase derivada, **ManualService**, que describe un servicio manual y una clase derivada, **autoservicio**, que describe un servicio automático. Ambas clases tienen un gran número de propiedades. No todas las propiedades son idénticas. Para cambiar un servicio de manual a automático, también debe cambiar la instancia que representa el servicio de **ManualService** a **autoservicio**. En la versión actual de WMI, no se puede llamar al método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) con el parámetro *PIN* que apunta a una instancia de **Autoservice** y a las propiedades de clave que describen la instancia de **ManualService** . Si lo hace, se elimina implícitamente la instancia de **ManualService** original. En esencia, después de establecer la clase de una instancia, solo se puede cambiar la clase primaria de una instancia mediante la eliminación de la instancia y volver a crear la instancia como una instancia de la nueva clase primaria.

En el procedimiento siguiente se describe cómo se mueve una instancia de una clase a otra.

**Para trasladar una instancia de una clase a otra**

1.  Elimine la instancia de la clase original.
2.  Cree la instancia en la nueva clase.

    WMI no permite que las aplicaciones muevan una instancia creando en la nueva clase y, a continuación, actualizándolos con la clave de la instancia original.

Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

 

 



