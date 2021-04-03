---
title: Crear un controlador de enlace
description: El programa cliente de una aplicación distribuida debe crear un identificador de enlace que indique el tiempo de ejecución de RPC en el que se debe establecer contacto con el servidor y cómo se debe establecer contacto con el servidor.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- RPC llamada a procedimiento remoto, tareas, crear un identificador de enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eddced351642d916f90cd5c127d0e51b764f7ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075426"
---
# <a name="creating-a-binding-handle"></a>Crear un controlador de enlace

El programa cliente de una aplicación distribuida debe crear un identificador de enlace que indique el tiempo de ejecución de RPC en el que se debe establecer contacto con el servidor y cómo se debe establecer contacto con el servidor.

En el fragmento de código siguiente se muestra un enfoque común para crear un identificador de enlace:


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



 

 




