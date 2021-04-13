---
description: 'Los métodos IWbemServices:: ExecMethod o ExecMethodAsync requieren la \_ \_ clase de sistema Parameters como contenedor en pInParams si el método que se está ejecutando tiene argumentos de entrada.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Crear objetos de parámetros en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276265"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="5b307-103">Crear objetos de parámetros en C++</span><span class="sxs-lookup"><span data-stu-id="5b307-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="5b307-104">Los métodos [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) requieren la clase de sistema [**\_ \_ Parameters**](--parameters.md) como contenedor en *pInParams* si el método que se está ejecutando tiene argumentos de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b307-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="5b307-105">En el procedimiento siguiente se describe cómo crear una instancia de la clase del sistema [**\_ \_ Parameters**](--parameters.md) para almacenar la información de parámetros.</span><span class="sxs-lookup"><span data-stu-id="5b307-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="5b307-106">**Para crear una instancia de \_ \_ parámetros**</span><span class="sxs-lookup"><span data-stu-id="5b307-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="5b307-107">Determine la ruta de acceso de la clase que contiene la definición del método.</span><span class="sxs-lookup"><span data-stu-id="5b307-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="5b307-108">Usar la ruta de acceso de clase y el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pasados desde [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), llamar a [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar las clases de parámetros de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="5b307-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="5b307-109">El método [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) devuelve un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para tener acceso a cada una de estas clases.</span><span class="sxs-lookup"><span data-stu-id="5b307-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="5b307-110">Con el puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para la clase de salida, llame a [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) para crear una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="5b307-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="5b307-111">Rellene la instancia de la clase estableciendo las propiedades que corresponden a los valores de salida y, si hay un valor devuelto para el método, la propiedad [ReturnValue](creating-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="5b307-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="5b307-112">Vuelva a pasar la instancia de [**\_ \_ parámetros**](--parameters.md) al llamador a través del método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="5b307-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="5b307-113">Una vez que un proveedor de métodos determina que los parámetros de entrada son correctos, el método al que apunta *strMethodName* podría seguir superándose o producir un error.</span><span class="sxs-lookup"><span data-stu-id="5b307-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="5b307-114">Algunos proveedores de métodos generan un segundo subproceso para implementar el método, de modo que el éxito o el error real del método terminen en informar al llamador a través de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="5b307-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="5b307-115">Tenga en cuenta que **IWbemObjectSink:: SetStatus** no recibe el código de retorno del método de proveedor.</span><span class="sxs-lookup"><span data-stu-id="5b307-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="5b307-116">Sin embargo, recibe el código de retorno del mecanismo de devolución de llamada real y solo es útil para comprobar que la llamada se produjo o que se produjo un error por motivos mecánicos.</span><span class="sxs-lookup"><span data-stu-id="5b307-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b307-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b307-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b307-118">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="5b307-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="5b307-119">**IWbemCallResult::GetResultObject**</span><span class="sxs-lookup"><span data-stu-id="5b307-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="5b307-120">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="5b307-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="5b307-121">**IWbemServices:: ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="5b307-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



