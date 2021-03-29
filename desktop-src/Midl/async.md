---
title: Async (atributo)
description: El atributo \ Async \ ACF define una llamada a procedimiento remoto como una operación asincrónica.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- atributo asincrónico MIDL
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995173"
---
# <a name="async-attribute"></a>Async (atributo)

El \[  \] atributo ACF Async define una llamada a procedimiento remoto como una operación asincrónica.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opt-ACF-atributos* 
</dt> <dd>

Especifica los atributos opcionales de configuración de la aplicación.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*lista de parámetros* 
</dt> <dd>

Especifica una lista de parámetros opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este atributo no es aplicable en las interfaces COM.

Para declarar una función RPC como asincrónica, primero declare la función como parte de una definición de interfaz en un archivo IDL. A continuación, modifique esa declaración de función en el archivo de configuración de la aplicación (ACF) aplicando el \[  \] atributo Async. Tenga en cuenta que la declaración de función no hace ninguna mención del identificador asincrónico y que el identificador de enlace es el primer parámetro. Al aplicar el \[ atributo **Async** \] en el archivo ACF, se genera el código adecuado de modo que, cuando se llama a esta función, el servidor asincrónico espera recibir un identificador asincrónico antes que los demás parámetros.

> [!Note]  
> El atributo Async no se puede usar con el modificador de la línea de comandos [**/OSF**](-osf.md) .

 

## <a name="examples"></a>Ejemplos

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[RPC asincrónico](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 