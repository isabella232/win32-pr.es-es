---
description: Define los parámetros de entrada y salida para los métodos.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697254"
---
# <a name="__parameters-class"></a><span data-ttu-id="4b672-103">\_\_Parameters (clase)</span><span class="sxs-lookup"><span data-stu-id="4b672-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="4b672-104">La clase de sistema **\_ \_ Parameters** es una clase abstracta que define los parámetros de entrada y salida para los métodos.</span><span class="sxs-lookup"><span data-stu-id="4b672-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="4b672-105">También se utiliza para pasar los valores de los parámetros de entrada y salida entre un cliente WMI y un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="4b672-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="4b672-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4b672-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4b672-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4b672-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b672-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b672-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="4b672-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b672-109">Members</span></span>

<span data-ttu-id="4b672-110">La clase **\_ \_ Parameters** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="4b672-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b672-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b672-111">Remarks</span></span>

<span data-ttu-id="4b672-112">Para definir un método en una clase de usuario, un cliente WMI crea una copia de la clase **\_ \_ Parameters** y agrega una propiedad para cada parámetro de entrada de un método.</span><span class="sxs-lookup"><span data-stu-id="4b672-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="4b672-113">Si el método contiene un valor devuelto o parámetros de salida, se debe crear otra copia de **\_ \_ los parámetros** .</span><span class="sxs-lookup"><span data-stu-id="4b672-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="4b672-114">Si el método devuelve un valor devuelto, el cliente debe agregar una propiedad denominada **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="4b672-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="4b672-115">A continuación, el proveedor de métodos almacena los parámetros de método con una llamada a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="4b672-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="4b672-116">Para invocar un método, un cliente llama a lo siguiente en secuencia:</span><span class="sxs-lookup"><span data-stu-id="4b672-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="4b672-117">[**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar una copia de la clase **\_ \_ Parameters** almacenada por [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="4b672-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="4b672-118">[**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)y, a continuación, establece una propiedad para cada parámetro de entrada para el método.</span><span class="sxs-lookup"><span data-stu-id="4b672-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="4b672-119">[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="4b672-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="4b672-120">Una vez finalizada la ejecución del método, se puede devolver otra instancia de la clase **\_ \_ Parameters** si el método tiene parámetros de salida o un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="4b672-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="4b672-121">Si el método se invocó mediante [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), la instancia de **\_ \_ Parameters** se devuelve como un argumento de salida.</span><span class="sxs-lookup"><span data-stu-id="4b672-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="4b672-122">Si el método se invocó mediante [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), la instancia de **\_ \_ Parameters** se devuelve como un parámetro a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="4b672-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b672-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b672-123">Requirements</span></span>



| <span data-ttu-id="4b672-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b672-124">Requirement</span></span> | <span data-ttu-id="4b672-125">Value</span><span class="sxs-lookup"><span data-stu-id="4b672-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4b672-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b672-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4b672-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b672-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4b672-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b672-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4b672-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b672-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4b672-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b672-130">Namespace</span></span><br/>                | <span data-ttu-id="4b672-131">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="4b672-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4b672-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b672-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b672-133">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4b672-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4b672-134">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="4b672-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="4b672-135">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="4b672-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




