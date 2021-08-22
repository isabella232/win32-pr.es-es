---
description: A diferencia de la eliminación de una instancia dinámica, la eliminación de una clase es un procedimiento simple.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Eliminar una clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad3e44292aa1ca6b534151a82f36df50802e04db788d8cfb8aaeb477c23164f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412095"
---
# <a name="deleting-a-class"></a>Eliminar una clase

A diferencia de la eliminación de una instancia dinámica, la eliminación de una clase es un procedimiento simple. Sin embargo, como se ha mencionado anteriormente, las clases base o derivadas rara vez se eliminan. En su lugar, una instancia se elimina más comúnmente. Scripting [API para WMI](scripting-api-for-wmi.md) usa los mismos métodos para eliminar un objeto de clase o una instancia. Para obtener más información, [vea Eliminación de una instancia de](deleting-an-instance.md). Para obtener información sobre cómo quitar clases e instancias del repositorio WMI, vea el comando [**pragma deleteclass**](pragma-deleteclass.md) de preprocesador.

La [API COM para WMI](com-api-for-wmi.md) tiene métodos diferentes para eliminar una instancia y eliminar un objeto .

En el procedimiento siguiente se describe cómo eliminar una clase base o una clase derivada.

**Para eliminar una clase base o una clase derivada**

-   Llame al [**método IWbemServices::D eleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) o [**IWbemServices::D eleteClassAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)

    Como sugiere el nombre, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) elimina una instancia de forma asincrónica mientras [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) elimina una instancia de forma sincrónica. Para usar **DeleteClassAsync,** también debe implementar un [**objeto IWbemObjectSink.**](iwbemobjectsink.md)

> [!Note]  
> Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que requiere el cliente, se recomienda usar la comunicación semisincronosa en lugar de la comunicación asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

 

 



