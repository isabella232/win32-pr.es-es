---
title: version (atributo)
description: El atributo \ version \ interface identifica una versión determinada entre varias versiones de una interfaz RPC. Con el atributo de versión, se asegura de que solo se permita el enlace de las versiones compatibles del software de cliente y servidor.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- atributo de versión MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076774"
---
# <a name="version-attribute"></a><span data-ttu-id="79b32-105">version (atributo)</span><span class="sxs-lookup"><span data-stu-id="79b32-105">version attribute</span></span>

<span data-ttu-id="79b32-106">El atributo de interfaz de **\[ versión \]** identifica una versión determinada entre varias versiones de una interfaz RPC.</span><span class="sxs-lookup"><span data-stu-id="79b32-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="79b32-107">Con el atributo de versión, se asegura de que solo se permita el enlace de las versiones compatibles del software de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="79b32-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="79b32-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79b32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79b32-109">*valor principal*</span><span class="sxs-lookup"><span data-stu-id="79b32-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="79b32-110">Especifica un entero corto sin signo entre cero y 65.535, ambos inclusive, que representa el número de la versión principal.</span><span class="sxs-lookup"><span data-stu-id="79b32-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="79b32-111">*valor secundario*</span><span class="sxs-lookup"><span data-stu-id="79b32-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="79b32-112">Especifica un entero corto sin signo entre cero y 65.535, ambos inclusive, que representa el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="79b32-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="79b32-113">El valor de la versión secundaria es opcional.</span><span class="sxs-lookup"><span data-stu-id="79b32-113">The minor version value is optional.</span></span> <span data-ttu-id="79b32-114">Si está presente, el valor de la versión secundaria está separado del número de versión principal por un carácter de punto (.).</span><span class="sxs-lookup"><span data-stu-id="79b32-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="79b32-115">Si no se especifica, el valor de la versión secundaria es cero.</span><span class="sxs-lookup"><span data-stu-id="79b32-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79b32-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79b32-116">Remarks</span></span>

<span data-ttu-id="79b32-117">El compilador MIDL no admite varias versiones de una interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="79b32-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="79b32-118">Como resultado, una lista de atributos de interfaz que incluye el atributo de **\[** [**objeto**](object.md) **\]** no puede incluir el atributo de **\[ versión \]** .</span><span class="sxs-lookup"><span data-stu-id="79b32-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="79b32-119">Para crear una nueva versión de una interfaz COM existente, utilice la herencia de interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="79b32-120">Una interfaz COM derivada tiene un UUID diferente, pero hereda las funciones miembro de interfaz, los códigos de estado y los atributos de interfaz de la interfaz base.</span><span class="sxs-lookup"><span data-stu-id="79b32-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="79b32-121">En combinación con el **\[** valor de [**UUID**](uuid.md) **\]** , el valor de la **\[ \] versión** identifica de forma única la interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="79b32-122">La biblioteca en tiempo de ejecución pasa los valores de la **\[ versión \]** y el **\[ UUID \]** al servidor cuando el cliente llama a una función remota.</span><span class="sxs-lookup"><span data-stu-id="79b32-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="79b32-123">Un cliente puede enlazar con un servidor para una interfaz determinada si:</span><span class="sxs-lookup"><span data-stu-id="79b32-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="79b32-124">El valor de **\[ UUID \]** es el mismo.</span><span class="sxs-lookup"><span data-stu-id="79b32-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="79b32-125">El número de versión principal es el mismo.</span><span class="sxs-lookup"><span data-stu-id="79b32-125">The major version number is the same.</span></span>
-   <span data-ttu-id="79b32-126">El número de versión secundaria del cliente es menor o igual que el número de versión secundaria del servidor.</span><span class="sxs-lookup"><span data-stu-id="79b32-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="79b32-127">Es la ventaja y el beneficio de los usuarios para mantener la compatibilidad ascendente entre versionsÂ, es decir, modificar la interfaz para que solo cambie el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="79b32-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="79b32-128">Puede conservar la compatibilidad ascendente al agregar nuevos tipos de datos que las funciones existentes no usan y al agregar nuevas funciones sin cambiar la especificación de interfaz para las funciones existentes.</span><span class="sxs-lookup"><span data-stu-id="79b32-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="79b32-129">Cambie el número de versión principal si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="79b32-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="79b32-130">Si cambia un tipo de datos utilizado por una función existente.</span><span class="sxs-lookup"><span data-stu-id="79b32-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="79b32-131">Si cambia la especificación de interfaz para una función existente (por ejemplo, agregando o quitando un parámetro).</span><span class="sxs-lookup"><span data-stu-id="79b32-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="79b32-132">Si agrega devoluciones de llamada a las que llaman las funciones existentes.</span><span class="sxs-lookup"><span data-stu-id="79b32-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="79b32-133">Cambie el número de versión secundaria si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="79b32-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="79b32-134">Si agrega definiciones de tipo o constantes que no se usan en ninguna función o devoluciones de llamada existentes.</span><span class="sxs-lookup"><span data-stu-id="79b32-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="79b32-135">Si no cambia ninguna función existente y agrega nuevas funciones a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="79b32-136">Si agrega devoluciones de llamada a las que no llama ninguna función existente y las nuevas devoluciones de llamada siguen las funciones existentes.</span><span class="sxs-lookup"><span data-stu-id="79b32-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="79b32-137">Si las modificaciones se cumplen como un cambio de compatibilidad ascendente de la interfaz, use el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="79b32-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="79b32-138">**Para modificar el archivo de interfaz (IDL)**</span><span class="sxs-lookup"><span data-stu-id="79b32-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="79b32-139">Agregue nuevas definiciones de constantes y tipos al archivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="79b32-140">Agregue funciones de devolución de llamada al final del archivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="79b32-141">Agregue nuevas funciones al final del archivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="79b32-142">El atributo **\[ version \]** puede aparecer como máximo una vez en el encabezado de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="79b32-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="79b32-143">Cuando el atributo de versión no está presente, la interfaz tiene una versión predeterminada de 0,0.</span><span class="sxs-lookup"><span data-stu-id="79b32-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="79b32-144">El carácter de punto entre los números principales y secundarios es un delimitador y no representa un separador decimal.</span><span class="sxs-lookup"><span data-stu-id="79b32-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="79b32-145">El número secundario se trata como un entero.</span><span class="sxs-lookup"><span data-stu-id="79b32-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="79b32-146">Los ceros a la izquierda no son significativos.</span><span class="sxs-lookup"><span data-stu-id="79b32-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="79b32-147">Los ceros a la derecha son significativos.</span><span class="sxs-lookup"><span data-stu-id="79b32-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="79b32-148">Por ejemplo, la configuración de versión 1,11 representa un valor principal de uno y un valor menor de once.</span><span class="sxs-lookup"><span data-stu-id="79b32-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="79b32-149">La versión 1,11 no representa un valor entre 1,1 y 1,2.</span><span class="sxs-lookup"><span data-stu-id="79b32-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="79b32-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="79b32-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b32-151">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="79b32-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="79b32-152">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="79b32-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="79b32-153">**objeto**</span><span class="sxs-lookup"><span data-stu-id="79b32-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="79b32-154">**uuid**</span><span class="sxs-lookup"><span data-stu-id="79b32-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




