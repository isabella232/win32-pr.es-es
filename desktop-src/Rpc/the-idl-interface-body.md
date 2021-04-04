---
title: Cuerpo de la interfaz IDL
description: El cuerpo de la interfaz IDL contiene tipos de datos que se utilizan en llamadas a procedimientos remotos y los prototipos de función para los procedimientos remotos.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792652"
---
# <a name="the-idl-interface-body"></a>Cuerpo de la interfaz IDL

El cuerpo de la interfaz IDL contiene tipos de datos que se utilizan en llamadas a procedimientos remotos y los prototipos de función para los procedimientos remotos. El cuerpo de la interfaz también puede contener importaciones, pragmas, declaraciones de constantes y declaraciones de tipos. En el modo de extensiones de Microsoft, el compilador MIDL también permite declaraciones implícitas en forma de definiciones de variables.

En el ejemplo siguiente se muestra un archivo IDL que contiene la definición de una interfaz. El cuerpo de la definición de interfaz, que se encuentra entre llaves, contiene la definición de una constante (**bufsize**), un tipo (**tipo de \_ identificador \_ de PCONTEXT**) y algunos procedimientos remotos **(RemoteOpen**, **RemoteRead**, **RemoteClose** y **Shutdown**).

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

Para obtener más información, vea la [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).

 

 