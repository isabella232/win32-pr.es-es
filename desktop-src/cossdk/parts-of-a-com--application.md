---
description: Las aplicaciones COM+ constan de uno o varios componentes COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Partes de una aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496025"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="c8a58-103">Partes de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="c8a58-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="c8a58-104">Las aplicaciones COM+ constan de uno o varios componentes COM.</span><span class="sxs-lookup"><span data-stu-id="c8a58-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="c8a58-105">Los siguientes términos se utilizan en toda la documentación de COM+:</span><span class="sxs-lookup"><span data-stu-id="c8a58-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="c8a58-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*</span><span class="sxs-lookup"><span data-stu-id="c8a58-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="c8a58-107">Unidad binaria de código que crea objetos COM (incluye el código de empaquetado y de registro).</span><span class="sxs-lookup"><span data-stu-id="c8a58-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="c8a58-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objeto COM*</span><span class="sxs-lookup"><span data-stu-id="c8a58-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="c8a58-109">Instancia de una clase COM.</span><span class="sxs-lookup"><span data-stu-id="c8a58-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="c8a58-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Clase COM*</span><span class="sxs-lookup"><span data-stu-id="c8a58-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="c8a58-111">Una implementación concreta y con nombre de una o más interfaces.</span><span class="sxs-lookup"><span data-stu-id="c8a58-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="c8a58-112">Una clase COM se identifica mediante un CLSID (a veces también mediante un ProgID).</span><span class="sxs-lookup"><span data-stu-id="c8a58-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="c8a58-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interfaz COM*</span><span class="sxs-lookup"><span data-stu-id="c8a58-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="c8a58-114">Grupo de funciones de método relacionadas expuestas por una clase COM que especifica un contrato.</span><span class="sxs-lookup"><span data-stu-id="c8a58-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="c8a58-115">Esto incluye el nombre, la firma de la interfaz, la semántica de la interfaz y el formato del búfer de serialización.</span><span class="sxs-lookup"><span data-stu-id="c8a58-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="c8a58-116">Un IID identifica una interfaz.</span><span class="sxs-lookup"><span data-stu-id="c8a58-116">An interface is identified by an IID.</span></span> <span data-ttu-id="c8a58-117">La sintaxis de la interfaz se define en las bibliotecas de tipos y de IDL.</span><span class="sxs-lookup"><span data-stu-id="c8a58-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="c8a58-118">Las interfaces de una clase COM se deben dividir en conjuntos de métodos coherentes y administrables.</span><span class="sxs-lookup"><span data-stu-id="c8a58-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="c8a58-119">Las interfaces COM son inmutables; el contrato COM indica que no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="c8a58-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="c8a58-120">Cualquier modificación (como agregar métodos) requiere la definición de una nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="c8a58-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="c8a58-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Método COM*</span><span class="sxs-lookup"><span data-stu-id="c8a58-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="c8a58-122">Uno de un conjunto de funciones relacionadas proporcionadas por una interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="c8a58-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="c8a58-123">Componentes configurados y no configurados</span><span class="sxs-lookup"><span data-stu-id="c8a58-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="c8a58-124">Para sacar partido de los servicios que admiten las aplicaciones COM+, el entorno COM+ impone requisitos específicos en los componentes COM compilados para aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="c8a58-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="c8a58-125">Cuando se agrega a una aplicación COM+, un componente COM se conoce como *componente configurado*.</span><span class="sxs-lookup"><span data-stu-id="c8a58-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="c8a58-126">Los componentes COM compilados para aplicaciones COM+ son componentes de servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="c8a58-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="c8a58-127">El componente debe contener una biblioteca de tipos (archivo. tlb) para describir todas las clases implementadas en el componente y declarar las interfaces en todas las clases del componente.</span><span class="sxs-lookup"><span data-stu-id="c8a58-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="c8a58-128">Puede crear e implementar estos componentes con Microsoft Visual Basic, Microsoft Visual C++ o cualquier herramienta de desarrollo compatible con COM.</span><span class="sxs-lookup"><span data-stu-id="c8a58-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="c8a58-129">Un *componente no configurado* es un componente que no está instalado en una aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="c8a58-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="c8a58-130">Puede transformar la mayoría de los componentes no configurados en componentes configurados simplemente mediante su integración en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="c8a58-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="c8a58-131">No use el mismo AppID para una aplicación COM+ y en el registro para un componente sin configurar.</span><span class="sxs-lookup"><span data-stu-id="c8a58-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="c8a58-132">Cuando se activa el componente sin configurar, como activación puede recuperar la información de la aplicación COM+ del registro que no contiene la información necesaria para la activación COM.</span><span class="sxs-lookup"><span data-stu-id="c8a58-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="c8a58-133">Pueden surgir problemas similares si se realiza una llamada a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) desde Dllhost que hospeda la aplicación de servidor com+.</span><span class="sxs-lookup"><span data-stu-id="c8a58-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
