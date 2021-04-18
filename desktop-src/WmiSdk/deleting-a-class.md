---
description: A diferencia de la eliminación de una instancia dinámica, la eliminación de una clase es un procedimiento sencillo.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Eliminar una clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706815"
---
# <a name="deleting-a-class"></a>Eliminar una clase

A diferencia de la eliminación de una instancia dinámica, la eliminación de una clase es un procedimiento sencillo. Sin embargo, como se explicó anteriormente, las clases base o derivadas rara vez se eliminan. En su lugar, una instancia se elimina más comúnmente. La [API de scripting para WMI](scripting-api-for-wmi.md) usa los mismos métodos para eliminar un objeto de clase o una instancia de. Para obtener más información, consulte [eliminar una instancia](deleting-an-instance.md). Para obtener información acerca de cómo quitar clases e instancias del repositorio WMI, vea el comando de preprocesador [**pragma deleteclass**](pragma-deleteclass.md) .

La [API de com para WMI](com-api-for-wmi.md) tiene distintos métodos para eliminar una instancia y eliminar un objeto.

En el procedimiento siguiente se describe cómo eliminar una clase base o una clase derivada.

**Para eliminar una clase base o una clase derivada**

-   Llame al método [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) o [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .

    Como sugiere el nombre, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) elimina una instancia de forma asincrónica, mientras que [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) elimina una instancia sincrónicamente. Para usar **DeleteClassAsync**, también debe implementar un objeto [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

 

 



