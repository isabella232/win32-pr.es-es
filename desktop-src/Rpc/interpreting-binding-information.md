---
title: Interpretar la información de enlace
description: Microsoft RPC permite que los programas de cliente y servidor tengan acceso a la información de un controlador de enlace e la interprete.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- RPC llamada a procedimiento remoto, tareas, interpretar enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487030"
---
# <a name="interpreting-binding-information"></a>Interpretar la información de enlace

Microsoft RPC permite que los programas de cliente y servidor tengan acceso a la información de un controlador de enlace e la interprete. Esto no significa que pueda o debe intentar acceder al contenido de un identificador de enlace directamente. Microsoft RPC proporciona funciones que establecen y recuperan la información en los identificadores de enlace.

Para obtener la información de un controlador de enlace, pase el identificador a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Devuelve la información de enlace como una cadena. Para cada llamada a **RpcBindingToStringBinding**, debe tener una llamada correspondiente a la función [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).

Puede llamar a la función [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para analizar la cadena que obtiene de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Esta función asigna cadenas para que contengan la información que analiza. Si no desea que analice una parte determinada de la información de enlace, pase un valor **null** como valor de ese parámetro. Asegúrese de llamar a [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para cada una de las cadenas que asigna.

En el fragmento de código siguiente se muestra cómo una aplicación puede llamar a estas funciones.


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



En el código de ejemplo anterior se llama a las funciones [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) y [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para obtener y analizar la información de un identificador de enlace válido. Tenga en cuenta que el valor **null** se pasó como segundo parámetro a **RpcStringBindingParse**. Esto hace que la función omita el análisis del UUID del objeto. Dado que no analiza el UUID, **RpcStringBindingParse** no asignará una cadena para él. Esta técnica permite que la aplicación solo asigne memoria para la información que le interesa analizar y analizar.

 

 




