---
title: Cuerpo de la interfaz IDL
description: El cuerpo de la interfaz IDL contiene tipos de datos usados en llamadas a procedimientos remotos y prototipos de función para los procedimientos remotos.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a25f1e74a1c0e33d0f3bde1318a36e8825fc350c445ee079ad534b67af51c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017065"
---
# <a name="the-idl-interface-body"></a>Cuerpo de la interfaz IDL

El cuerpo de la interfaz IDL contiene tipos de datos usados en llamadas a procedimientos remotos y prototipos de función para los procedimientos remotos. El cuerpo de la interfaz también puede contener importaciones, pragmas, declaraciones constantes y declaraciones de tipo. En el modo de extensiones de Microsoft, el compilador MIDL también permite declaraciones implícitas en forma de definiciones de variables.

En el ejemplo siguiente se muestra un archivo IDL que contiene la definición de una interfaz. El cuerpo de la definición de interfaz, que se produce entre los corchetes, contiene la definición de una constante (**BUFSIZE**), un tipo (**PCONTEXT \_ HANDLE \_ TYPE**) y algunos procedimientos remotos **(RemoteOpen,** **RemoteRead,** **RemoteClose** y **Shutdown).**

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

Para obtener más información, vea la [referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).

 

 