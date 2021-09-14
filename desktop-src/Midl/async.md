---
title: atributo asincrónico
description: El atributo \async\ ACF define una llamada a procedimiento remoto como una operación asincrónica.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL de atributo asincrónico
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159671"
---
# <a name="async-attribute"></a>atributo asincrónico

El \[ **atributo ACF** \] asincrónico define una llamada a procedimiento remoto como una operación asincrónica.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opt-acf-attributes* 
</dt> <dd>

Especifica atributos de configuración de aplicación opcionales.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*param-list* 
</dt> <dd>

Especifica una lista de parámetros opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este atributo no es aplicable en las interfaces COM.

Para declarar una función RPC como asincrónica, declare primero la función como parte de una definición de interfaz en un archivo IDL. A continuación, modifique esa declaración de función, dentro del archivo de configuración de la aplicación (ACF), aplicando el \[ **atributo** \] asincrónico. Tenga en cuenta que la declaración de función no hace ninguna mención al identificador asincrónico y que el identificador de enlace es el primer parámetro. La aplicación del atributo asincrónico en el archivo ACF genera el código adecuado para que, cuando se llama a esta función, el servidor asincrónico espere recibir un identificador asincrónico antes que los demás \[  \] parámetros.

> [!Note]  
> El atributo asincrónico no se puede usar con el modificador de línea de comandos [**/osf.**](-osf.md)

 

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

[RPC asincrónica](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 