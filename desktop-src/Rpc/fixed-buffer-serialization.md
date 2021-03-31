---
title: Serialización de búfer fijo
description: Serialización de búfer fija.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418780"
---
# <a name="fixed-buffer-serialization"></a>Serialización de búfer fijo

Cuando use el estilo de búfer fijo, especifique un búfer lo suficientemente grande como para alojar las operaciones de codificación (serialización) realizadas con el identificador. Al anular la serialización, se proporciona el búfer que contiene todos los datos que se van a descodificar.

El estilo de búfer fijo de serialización utiliza las siguientes rutinas:

-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La función **MesEncodeFixedBufferHandleCreate** asigna la memoria necesaria para el controlador de codificación y, a continuación, la inicializa. La aplicación puede llamar a [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar el identificador, o puede llamar a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar la memoria del controlador. Para crear un identificador de descodificación que se corresponda con el identificador de codificación de estilo fijo, debe utilizar [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

La aplicación llama a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar el identificador de búfer de codificación o descodificación.

## <a name="examples-of-fixed-buffer-encoding"></a>Ejemplos de codificación de búfer fija

En la sección siguiente se proporciona un ejemplo de cómo usar un estilo de búfer fijo: serialización de un identificador para la codificación de procedimientos.

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

El siguiente fragmento representa una parte de una aplicación.

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

En la sección siguiente se proporciona un ejemplo de cómo usar un estilo de búfer fijo: serialización de un controlador para la codificación de tipos.

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

El siguiente fragmento representa los fragmentos de aplicación pertinentes.


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




