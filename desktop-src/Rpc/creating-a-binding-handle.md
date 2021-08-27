---
title: Crear un identificador de enlace
description: El programa cliente de una aplicación distribuida debe crear un identificador de enlace que indique al tiempo de ejecución rpc qué servidor debe ponerse en contacto y cómo se debe ponerse en contacto con el servidor.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- Llamada a procedimiento remoto RPC, tareas, creación de un identificador de enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b1d805a765649f640ff10f8cb825264e3402c8938786d183b0be351036c971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101715"
---
# <a name="creating-a-binding-handle"></a>Crear un identificador de enlace

El programa cliente de una aplicación distribuida debe crear un identificador de enlace que indique al tiempo de ejecución rpc qué servidor debe ponerse en contacto y cómo se debe ponerse en contacto con el servidor.

El fragmento de código siguiente muestra un enfoque común para crear un identificador de enlace:


```C++
RPC_STATUS status;
unsigned short *StringBinding;
RPC_BINDING_HANDLE BindingHandle;
status = RpcStringBindingCompose(NULL,  // Object UUID
             L"ncacn_ip_tcp",           // Protocol sequence to use
             L"MyServer.MyCompany.com", // Server DNS or Netbios Name
             NULL,
             NULL,
             &StringBinding);
// Error checking ommitted. If no error, we proceed below
status = RpcBindingFromStringBinding(StringBinding, &BindingHandle);

// free string regardless of errors from RpcBindingFromStringBinding
RpcStringFree(&StringBinding);

// Error checking ommitted. If no error, we have a valid binding handle
```



 

 




