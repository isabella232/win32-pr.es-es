---
title: modificador/OSF
description: El conmutador/OSF fuerza la compatibilidad estricta con el DCE de OSF.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /OSF modificador MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077637"
---
# <a name="osf-switch"></a><span data-ttu-id="97337-104">modificador/OSF</span><span class="sxs-lookup"><span data-stu-id="97337-104">/osf switch</span></span>

<span data-ttu-id="97337-105">El conmutador **/OSF** fuerza la compatibilidad estricta con el DCE de OSF.</span><span class="sxs-lookup"><span data-stu-id="97337-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="97337-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="97337-106">Switch Options</span></span>

<span data-ttu-id="97337-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="97337-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="97337-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97337-108">Remarks</span></span>

<span data-ttu-id="97337-109">Use este modificador si la aplicación requiere una compatibilidad estricta con OSF DCE por motivos de portabilidad.</span><span class="sxs-lookup"><span data-stu-id="97337-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="97337-110">En el modo **/OSF** , el paquete RPCSS se habilita automáticamente cuando se usan punteros completos, los argumentos requieren la asignación de memoria o cuando se usa el atributo [**enable \_ allocate**](enable-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="97337-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="97337-111">Esto significa que no es necesario proporcionar las funciones de [**\_ \_ asignación**](/windows/desktop/Rpc/the-midl-user-allocate-function) de usuarios de MIDL y de [**\_ \_ usuario de MIDL**](/windows/desktop/Rpc/the-midl-user-free-function) en la aplicación de cliente y de servidor.</span><span class="sxs-lookup"><span data-stu-id="97337-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="97337-112">Las siguientes características extendidas de Microsoft no están disponibles al compilar con el modificador **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="97337-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="97337-113">Declaradores abstractos (parámetros sin nombre) en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="97337-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="97337-114">Definiciones de interfaz para objetos COM.</span><span class="sxs-lookup"><span data-stu-id="97337-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="97337-115">Nombres de interfaz con más de 17 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97337-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="97337-116">Atributos de solo MIDL, como las [**\_ referencias de conexión**](wire-marshal.md), las [**\_ referencias de usuario**](user-marshal.md)y las extensiones typelib (ODL).</span><span class="sxs-lookup"><span data-stu-id="97337-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="97337-117">Usar palabras clave ACF en un archivo IDL (la opción de **\_ configuración/App** de MIDL).</span><span class="sxs-lookup"><span data-stu-id="97337-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="97337-118">Funciones de devolución de llamada estáticas en el cliente.</span><span class="sxs-lookup"><span data-stu-id="97337-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="97337-119">Atributo [**Async**](async.md) .</span><span class="sxs-lookup"><span data-stu-id="97337-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="97337-120">[**CPP \_ Quote**](cpp-quote.md) y **\# pragma MIDL \_ echo**.</span><span class="sxs-lookup"><span data-stu-id="97337-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="97337-121">tipos de caracteres anchos, constantes y cadenas de [**WCHAR \_ t**](wchar-t.md) .</span><span class="sxs-lookup"><span data-stu-id="97337-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="97337-122">inicialización de [**enumeración**](enum.md) (enumeradores dispersos).</span><span class="sxs-lookup"><span data-stu-id="97337-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="97337-123">Especificación de tamaño de solo [**salida**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="97337-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="97337-124">Punteros de tamaño mixto y matrices de tamaño.</span><span class="sxs-lookup"><span data-stu-id="97337-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="97337-125">Expresiones usadas para los especificadores de tamaño y discriminador.</span><span class="sxs-lookup"><span data-stu-id="97337-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="97337-126">Parámetros de identificador explícitos en cualquier posición de la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="97337-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="97337-127">En el modo **/OSF** , el compilador MIDL busca un identificador de enlace explícito como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="97337-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="97337-128">Cuando el primer parámetro no es un identificador de enlace y se especifican uno o más identificadores de contexto, se usa el identificador de contexto situado más a la izquierda como identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="97337-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="97337-129">Cuando el primer parámetro no es un identificador y no hay identificadores de contexto, el procedimiento utiliza el enlace implícito mediante el [**\_ identificador implícito**](implicit-handle.md) del atributo ACF o el [**\_ identificador automático**](auto-handle.md).</span><span class="sxs-lookup"><span data-stu-id="97337-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="97337-130">Herencia de tipos de atributos de puntero.</span><span class="sxs-lookup"><span data-stu-id="97337-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="97337-131">OSF DCE no permite punteros sin atributos.</span><span class="sxs-lookup"><span data-stu-id="97337-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="97337-132">Por lo tanto, en el modo **/OSF** cada archivo IDL debe definir atributos para sus punteros.</span><span class="sxs-lookup"><span data-stu-id="97337-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="97337-133">Si un puntero no tiene un atributo explícito, el archivo IDL debe tener una especificación [**\_ predeterminada de puntero**](pointer-default.md) para establecer el tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="97337-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="97337-134">Varias interfaces en un archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="97337-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="97337-135">Definiciones fuera del bloque de interfaz.</span><span class="sxs-lookup"><span data-stu-id="97337-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="97337-136">Calificadores de tipo, como **Far** y **Stdcall**.</span><span class="sxs-lookup"><span data-stu-id="97337-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="97337-137">Omitir atributos direccionales.</span><span class="sxs-lookup"><span data-stu-id="97337-137">Omitting directional attributes.</span></span>

<span data-ttu-id="97337-138">Las siguientes extensiones del lenguaje C/C++ no están disponibles al compilar con el modificador **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="97337-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="97337-139">Campos de bits en estructuras y uniones.</span><span class="sxs-lookup"><span data-stu-id="97337-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="97337-140">Comentarios de una sola línea delimitados con dos caracteres de barra diagonal (//).</span><span class="sxs-lookup"><span data-stu-id="97337-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="97337-141">Declaraciones externas.</span><span class="sxs-lookup"><span data-stu-id="97337-141">External declarations.</span></span>
-   <span data-ttu-id="97337-142">Procedimientos con puntos suspensivos en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="97337-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="97337-143">Escriba [**int**](int.md).</span><span class="sxs-lookup"><span data-stu-id="97337-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="97337-144">Escriba **void \*** (excepto con el atributo de [**\_ identificador de contexto**](context-handle.md) ).</span><span class="sxs-lookup"><span data-stu-id="97337-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="97337-145">Los calificadores de tipo, incluido el formulario con el prefijo compatible con ANSI, contienen dos caracteres de subrayado: **\_ \_ Cdecl**, **Cdecl**, [**const**](const.md), **const**, **\_ \_ Export**, **Export**, **\_ \_ Far**, **Far**, **\_ \_ loadds**, **loadds**, **\_ \_ Near**, **Near**, **\_ \_ Pascal**, **Pascal**, **\_ \_ Stdcall**, **Stdcall**, **\_ \_ volatile** y **volatile**.</span><span class="sxs-lookup"><span data-stu-id="97337-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="97337-146">Cualquier \# Advertencia [**pragma**](pragma.md) o comentario **\# pragma** .</span><span class="sxs-lookup"><span data-stu-id="97337-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="97337-147">Serialización de tipo.</span><span class="sxs-lookup"><span data-stu-id="97337-147">Type serialization.</span></span>
-   <span data-ttu-id="97337-148">El tipo de datos [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="97337-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="97337-149">El modificador [**/Protocolo**](-protocol.md) y la sintaxis de transferencia ndr64.</span><span class="sxs-lookup"><span data-stu-id="97337-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="97337-150">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="97337-150">Examples</span></span>

<span data-ttu-id="97337-151">**MIDL/OSF nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="97337-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="97337-152">**MIDL/OSF/APP \_ config nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="97337-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="97337-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="97337-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97337-154">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="97337-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="97337-155">**configuración de/APP \_**</span><span class="sxs-lookup"><span data-stu-id="97337-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="97337-156">**\_ext/MS**</span><span class="sxs-lookup"><span data-stu-id="97337-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="97337-157">Paquete de administración de memoria RPCSS</span><span class="sxs-lookup"><span data-stu-id="97337-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 