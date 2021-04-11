---
description: El propósito del contenedor del proveedor es encapsular y usar las interfaces COM de bajo nivel (proporcionadas por los fabricantes de tarjetas inteligentes) para una tarjeta inteligente determinada. Microsoft no proporciona estas interfaces.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Proveedor de servicios de contenedor de proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154140"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="4c88f-104">Proveedor de servicios de contenedor de proveedores</span><span class="sxs-lookup"><span data-stu-id="4c88f-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="4c88f-105">El propósito del contenedor del proveedor es encapsular y usar las interfaces COM de bajo nivel (proporcionadas por los fabricantes de tarjetas inteligentes) para una tarjeta inteligente determinada.</span><span class="sxs-lookup"><span data-stu-id="4c88f-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="4c88f-106">Microsoft no proporciona estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="4c88f-106">These interfaces are not supplied by Microsoft.</span></span>

![contenedor de proveedores](images/scspart1.png)

<span data-ttu-id="4c88f-108">Tal como se describe en la parte 6 de la *especificación de interoperabilidad para ICCS y los sistemas informáticos personales* (consulte las especificaciones en [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ), la funcionalidad expuesta por este contenedor es más fácil de usar que la funcionalidad de cuatro proveedores de servicios independientes.</span><span class="sxs-lookup"><span data-stu-id="4c88f-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="4c88f-109">La funcionalidad del contenedor se puede dividir en cuatro áreas principales:</span><span class="sxs-lookup"><span data-stu-id="4c88f-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="4c88f-110">Servicios de autenticación de tarjeta inteligente, como obtener desafío y autenticación de tarjeta.</span><span class="sxs-lookup"><span data-stu-id="4c88f-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="4c88f-111">Acceso a archivos de tarjeta inteligente o servicios del sistema de archivos, como abrir, cerrar, leer y escribir.</span><span class="sxs-lookup"><span data-stu-id="4c88f-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="4c88f-112">Administración de tarjetas inteligentes, como adjuntar y separar.</span><span class="sxs-lookup"><span data-stu-id="4c88f-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="4c88f-113">Servicios de comprobación de tarjetas inteligentes, como comprobar y cambiar código.</span><span class="sxs-lookup"><span data-stu-id="4c88f-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="4c88f-114">Esta especificación puede no estar disponible en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="4c88f-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="4c88f-115">La funcionalidad es específica del tipo de tarjeta que se va a usar (qué funciones admite la tarjeta, protocolos, etc.) y será diferente para cada tarjeta.</span><span class="sxs-lookup"><span data-stu-id="4c88f-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="4c88f-116">El contenedor de ejemplo de Microsoft SCardCOM utiliza la biblioteca COM ATL para implementar un contenedor simple y diseñar una plantilla para otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="4c88f-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="4c88f-117">Implementa las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="4c88f-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="4c88f-118">Interfaz u objeto</span><span class="sxs-lookup"><span data-stu-id="4c88f-118">Interface or object</span></span>                                     | <span data-ttu-id="4c88f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c88f-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="4c88f-120">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="4c88f-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="4c88f-121">Servicios de autenticación.</span><span class="sxs-lookup"><span data-stu-id="4c88f-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="4c88f-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="4c88f-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="4c88f-123">Servicios del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4c88f-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="4c88f-124">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="4c88f-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="4c88f-125">Servicios de administración.</span><span class="sxs-lookup"><span data-stu-id="4c88f-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="4c88f-126">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="4c88f-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="4c88f-127">Servicios de comprobación.</span><span class="sxs-lookup"><span data-stu-id="4c88f-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="4c88f-128">El ejemplo SCardCOM se proporciona únicamente como ejemplo de implementación de las interfaces contenedoras.</span><span class="sxs-lookup"><span data-stu-id="4c88f-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="4c88f-129">Para evitar el conflicto de nombres de DLL con otros proveedores, no debe utilizar SCardCOM.dll como nombre de los archivos DLL que cree.</span><span class="sxs-lookup"><span data-stu-id="4c88f-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="4c88f-130">El siguiente es un uso típico del contenedor del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4c88f-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="4c88f-131">En este ejemplo se utiliza la interfaz [**ISCardManage**](iscardmanage.md) para crear instancias de las interfaces que se van a encapsular en el proveedor de servicios y la interfaz [**ISCardVerify**](iscardverify.md) para comprobar su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="4c88f-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="4c88f-132">**Para compilar un proveedor de servicios de contenedor**</span><span class="sxs-lookup"><span data-stu-id="4c88f-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="4c88f-133">Cree una instancia de la interfaz [**ISCardManage**](iscardmanage.md) .</span><span class="sxs-lookup"><span data-stu-id="4c88f-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="4c88f-134">Use esta interfaz para crear una instancia de interfaces requeridas (por ejemplo, [**ISCardFileAccess**](iscardfileaccess.md) o [**ISCardVerify**](iscardverify.md)).</span><span class="sxs-lookup"><span data-stu-id="4c88f-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="4c88f-135">Al crear estas interfaces, también se crearán las interfaces COM de bajo nivel correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4c88f-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="4c88f-136">Adjunte o conéctese a una tarjeta a través del método [**ISCardManage**](iscardmanage.md) adecuado.</span><span class="sxs-lookup"><span data-stu-id="4c88f-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="4c88f-137">Realizar las operaciones necesarias a través del método [**ISCardVerify**](iscardverify.md) adecuado (que puede llamar a varios métodos y interfaces com de bajo nivel para completarse).</span><span class="sxs-lookup"><span data-stu-id="4c88f-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="4c88f-138">Repita el procedimiento para otras operaciones.</span><span class="sxs-lookup"><span data-stu-id="4c88f-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="4c88f-139">Liberar al finalizar.</span><span class="sxs-lookup"><span data-stu-id="4c88f-139">Release when complete.</span></span>

<span data-ttu-id="4c88f-140">El nombre de la interfaz COM y el identificador de interfaz (GUID) no deben cambiar de los utilizados en el contenedor de código o de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4c88f-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="4c88f-141">Sin embargo, el GUID de clase (es decir, donde reside una implementación real de una interfaz) debe cambiarse de los usados.</span><span class="sxs-lookup"><span data-stu-id="4c88f-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="4c88f-142">Esto es especialmente importante cuando se implementa un contenedor de proveedores.</span><span class="sxs-lookup"><span data-stu-id="4c88f-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="4c88f-143">Un ejemplo sería el uso de varios contenedores de proveedor en un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="4c88f-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="4c88f-144">Estos contenedores deben implementar las mismas interfaces COM, pero siempre usarán distintas estrategias de implementación.</span><span class="sxs-lookup"><span data-stu-id="4c88f-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="4c88f-145">Por lo tanto, se requieren diferentes clases (y identificadores de clase).</span><span class="sxs-lookup"><span data-stu-id="4c88f-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




