---
title: Implementación de una interfaz principal del proveedor de instancias
description: Un proveedor de instancias usa los métodos asincrónicos de IWbemServices como interfaz principal para WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8157a7b4e9637314eb8bb09cdb34e2d3d1d9c87202e6ad0ea4b08fddd3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108559"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Implementación de una interfaz principal del proveedor de instancias

Un proveedor de instancias usa los métodos [**asincrónicos de IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como interfaz principal para WMI. Al implementar solo los métodos que satisfacen las necesidades del proveedor de instancias, puede reducir la cantidad de recursos que dedica a codificar. Sin embargo, al implementar métodos reservados para otros tipos de proveedores, puede reducir el número de proveedores que escribe.

Dado que también lo usan aplicaciones y proveedores para solicitar servicios de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contiene muchos métodos que son irrelevantes para un proveedor de instancias. En la tabla siguiente se enumeran **los métodos IWbemServices** que puede implementar para un proveedor de instancias.



| Método                                                                   | Característica          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Recuperación        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Modificación     |
| [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Eliminación         |
| [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Enumeración      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Procesamiento de consultas |



 

Para los métodos que no use, el proveedor puede proporcionar una implementación de código auxiliar que devuelva **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE**. Esto incluye todos [**los métodos IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que no aparecen en la tabla anterior.

Un único proveedor puede actuar simultáneamente como proveedor de clases, instancias y métodos mediante el registro y la implementación adecuados de todos los métodos pertinentes. Para obtener más información, vea [Escribir un proveedor de clases y](writing-a-class-provider.md) Escribir un proveedor de [métodos](writing-a-method-provider.md).

 

 



