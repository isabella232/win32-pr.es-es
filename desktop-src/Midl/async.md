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
# <a name="async-attribute"></a><span data-ttu-id="b8dce-104">Async (atributo)</span><span class="sxs-lookup"><span data-stu-id="b8dce-104">async attribute</span></span>

<span data-ttu-id="b8dce-105">El \[  \] atributo ACF Async define una llamada a procedimiento remoto como una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b8dce-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="b8dce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8dce-107">*opt-ACF-atributos*</span><span class="sxs-lookup"><span data-stu-id="b8dce-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="b8dce-108">Especifica los atributos opcionales de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8dce-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="b8dce-109">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="b8dce-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b8dce-110">Especifica el nombre de la función en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b8dce-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="b8dce-111">*lista de parámetros*</span><span class="sxs-lookup"><span data-stu-id="b8dce-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b8dce-112">Especifica una lista de parámetros opcional.</span><span class="sxs-lookup"><span data-stu-id="b8dce-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8dce-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8dce-113">Remarks</span></span>

<span data-ttu-id="b8dce-114">Este atributo no es aplicable en las interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="b8dce-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="b8dce-115">Para declarar una función RPC como asincrónica, primero declare la función como parte de una definición de interfaz en un archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b8dce-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="b8dce-116">A continuación, modifique esa declaración de función en el archivo de configuración de la aplicación (ACF) aplicando el \[  \] atributo Async.</span><span class="sxs-lookup"><span data-stu-id="b8dce-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="b8dce-117">Tenga en cuenta que la declaración de función no hace ninguna mención del identificador asincrónico y que el identificador de enlace es el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="b8dce-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="b8dce-118">Al aplicar el \[ atributo **Async** \] en el archivo ACF, se genera el código adecuado de modo que, cuando se llama a esta función, el servidor asincrónico espera recibir un identificador asincrónico antes que los demás parámetros.</span><span class="sxs-lookup"><span data-stu-id="b8dce-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="b8dce-119">El atributo Async no se puede usar con el modificador de la línea de comandos [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="b8dce-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b8dce-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8dce-120">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b8dce-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8dce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8dce-122">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="b8dce-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="b8dce-123">RPC asincrónico</span><span class="sxs-lookup"><span data-stu-id="b8dce-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 