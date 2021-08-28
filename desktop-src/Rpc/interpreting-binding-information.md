---
title: Interpretación de la información de enlace
description: Microsoft RPC permite que los programas de cliente y servidor accedan a la información de un identificador de enlace e interpreten la información.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Remote Procedure Call RPC , tasks, interpreting binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5578683b06ac75b99e2865d55512449ad2217984234a9bf9d3cf7e8360c053e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020385"
---
# <a name="interpreting-binding-information"></a>Interpretación de la información de enlace

Microsoft RPC permite que los programas de cliente y servidor accedan a la información de un identificador de enlace e interpreten la información. Esto no significa que pueda o deba intentar acceder directamente al contenido de un identificador de enlace. Rpc de Microsoft proporciona funciones que establecen y recuperan la información en los identificadores de enlace.

Para obtener la información de un identificador de enlace, pase el identificador a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Devuelve la información de enlace como una cadena. Para cada llamada a **RpcBindingToStringBinding**, debe tener una llamada correspondiente a la [**función RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).

Puede llamar a la [**función RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para analizar la cadena que se obtiene de [**RpcBindingToStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) Esta función asigna cadenas para contener la información que analiza. Si no desea que analice una parte determinada de la información de enlace, pase un **valor NULL** como valor de ese parámetro. Asegúrese de llamar a [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para cada una de las cadenas que asigna.

En el fragmento de código siguiente se muestra cómo una aplicación podría llamar a estas funciones.


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



El código de ejemplo anterior llama a las funciones [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) y [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) para obtener y analizar la información en un identificador de enlace válido. Tenga en cuenta que **el valor NULL** se pasó como segundo parámetro a **RpcStringBindingParse.** Esto hace que esa función omita el análisis del UUID del objeto. Puesto que no analiza el UUID, **RpcStringBindingParse** no le asignará una cadena. Esta técnica permite que la aplicación solo asigne memoria para la información que le interesa analizar y analizar.

 

 




