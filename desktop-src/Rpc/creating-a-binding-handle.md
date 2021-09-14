---
title: Crear un identificador de enlace
description: El programa cliente de una aplicación distribuida debe crear un identificador de enlace que indique al tiempo de ejecución de RPC qué servidor debe ponerse en contacto y cómo se debe ponerse en contacto con el servidor.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- Llamada a procedimiento remoto RPC , tareas, creación de un identificador de enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eddced351642d916f90cd5c127d0e51b764f7ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259836"
---
# <a name="creating-a-binding-handle"></a>Crear un identificador de enlace

El programa cliente de una aplicación distribuida debe crear un identificador de enlace que indique al tiempo de ejecución de RPC qué servidor debe ponerse en contacto y cómo se debe ponerse en contacto con el servidor.

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



 

 




