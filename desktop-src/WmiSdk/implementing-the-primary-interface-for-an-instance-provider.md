---
title: Implementar una interfaz principal de proveedor de instancias
description: Un proveedor de instancias utiliza los métodos asincrónicos de IWbemServices como la interfaz principal para WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716555"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Implementar una interfaz principal de proveedor de instancias

Un proveedor de instancias utiliza los métodos asincrónicos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal para WMI. Al implementar solo los métodos que satisfacen las necesidades de su proveedor de instancias, puede reducir la cantidad de recursos que emplea para codificar. Sin embargo, mediante la implementación de métodos reservados para otros tipos de proveedores, puede reducir el número de proveedores que escribe.

Dado que las aplicaciones y los proveedores también lo utilizan para solicitar servicios de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contiene muchos métodos que son irrelevantes para un proveedor de instancias. En la tabla siguiente se enumeran los métodos **IWbemServices** que se pueden implementar para un proveedor de instancias.



| Método                                                                   | Característica          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Recuperación        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Modificación     |
| [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Eliminación         |
| [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Enumeración      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Procesamiento de consultas |



 

En el caso de los métodos que no use, el proveedor puede proporcionar una implementación de código auxiliar que devuelva el **proveedor de WBEM \_ E \_ \_ no \_ compatible**. Esto incluye todos los métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que no aparecen en la tabla anterior.

Un único proveedor puede actuar simultáneamente como una clase, una instancia y un proveedor de métodos mediante el registro y la implementación correctos de todos los métodos pertinentes. Para obtener más información, vea [escribir un proveedor de clases](writing-a-class-provider.md) y [escribir un proveedor de métodos](writing-a-method-provider.md).

 

 



