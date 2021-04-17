---
description: Cuando se utiliza la seguridad basada en roles en la aplicación COM+ que contiene el componente, se tiene acceso a la funcionalidad de seguridad mediante programación desde dentro del componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Seguridad de componentes mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705321"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="78ea6-103">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="78ea6-103">Programmatic Component Security</span></span>

<span data-ttu-id="78ea6-104">Cuando se utiliza la seguridad basada en roles en la aplicación COM+ que contiene el componente, se tiene acceso a la funcionalidad de seguridad mediante programación desde dentro del componente.</span><span class="sxs-lookup"><span data-stu-id="78ea6-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="78ea6-105">Puede comprobar la pertenencia al rol para determinar si se ejecutan determinadas secciones de código, puede tener acceso a la información de seguridad mediante el objeto de contexto de llamada de seguridad, y puede determinar si la seguridad está habilitada para la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="78ea6-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="78ea6-106">Puede realizar todas estas tareas mediante una referencia a un objeto [**SecurityCallContext**](securitycallcontext.md) (para aplicaciones de Microsoft Visual Basic) o un puntero a la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (para aplicaciones de C y Microsoft Visual C++).</span><span class="sxs-lookup"><span data-stu-id="78ea6-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="78ea6-107">Para obtener más información sobre la seguridad basada en roles mediante programación, vea los temas siguientes en esta sección:</span><span class="sxs-lookup"><span data-stu-id="78ea6-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="78ea6-108">Comprobando la pertenencia al rol</span><span class="sxs-lookup"><span data-stu-id="78ea6-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="78ea6-109">Determinar si está habilitada la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="78ea6-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="78ea6-110">Obtener acceso a la información de contexto de llamada de seguridad</span><span class="sxs-lookup"><span data-stu-id="78ea6-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="78ea6-111">Características de suplantación y seguridad COM</span><span class="sxs-lookup"><span data-stu-id="78ea6-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="78ea6-112">Si el componente se utiliza en una aplicación COM+ que no usa la seguridad basada en roles, la comprobación de roles mediante programación y la información de contexto de llamada de seguridad no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="78ea6-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="78ea6-113">Sin embargo, puede utilizar la funcionalidad de seguridad mediante programación proporcionada por COM.</span><span class="sxs-lookup"><span data-stu-id="78ea6-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="78ea6-114">Para obtener más información, vea [seguridad en com](/windows/desktop/com/security-in-com).</span><span class="sxs-lookup"><span data-stu-id="78ea6-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="78ea6-115">Aunque puede usar la mayoría de las funciones de seguridad proporcionadas por COM, no se puede llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) desde un componente que forma parte de una aplicación com+ porque el suplente al que se ejecuta la aplicación com+ llama a **CoInitializeSecurity** .</span><span class="sxs-lookup"><span data-stu-id="78ea6-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="78ea6-116">Sin embargo, puede llamar a otras funciones de seguridad, como [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), que recupera información sobre el cliente.</span><span class="sxs-lookup"><span data-stu-id="78ea6-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="78ea6-117">En concreto, cuando necesite usar la identidad del cliente para tener acceso a algún recurso (por ejemplo, tener acceso a un archivo protegido por un descriptor de seguridad o propagar la identidad del cliente a través de una base de datos), puede realizar la suplantación mediante programación.</span><span class="sxs-lookup"><span data-stu-id="78ea6-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="78ea6-118">Para obtener más información sobre cuándo y cómo hacerlo, vea [suplantación y delegación de cliente](client-impersonation-and-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="78ea6-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="78ea6-119">Probar la funcionalidad de seguridad</span><span class="sxs-lookup"><span data-stu-id="78ea6-119">Testing Security Functionality</span></span>

<span data-ttu-id="78ea6-120">Si utiliza la seguridad de programación de COM+ en el componente, debe integrar el componente en una aplicación COM+ cuando esté listo para probar la funcionalidad de seguridad del componente.</span><span class="sxs-lookup"><span data-stu-id="78ea6-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="78ea6-121">Si un componente que utiliza la seguridad mediante programación de COM+ se ejecuta sin integrarse en una aplicación COM+, se producirán excepciones.</span><span class="sxs-lookup"><span data-stu-id="78ea6-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="78ea6-122">Por lo tanto, si desea asegurarse de que este componente también sea capaz de integrarse correctamente en una aplicación que no forma parte del entorno de COM+, debe asegurarse de que estas excepciones se controlen correctamente.</span><span class="sxs-lookup"><span data-stu-id="78ea6-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="78ea6-123">Documentar los requisitos de seguridad</span><span class="sxs-lookup"><span data-stu-id="78ea6-123">Documenting Security Requirements</span></span>

<span data-ttu-id="78ea6-124">Si está escribiendo un componente independiente para aplicaciones COM+ que usan la seguridad basada en roles, debe documentar el componente para que la seguridad se pueda configurar correctamente cuando el componente se integre en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="78ea6-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="78ea6-125">Por ejemplo, debe identificar los roles que se deben agregar y explicar a qué métodos e interfaces se debe asignar cada rol.</span><span class="sxs-lookup"><span data-stu-id="78ea6-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="78ea6-126">Además, si se llama a un método como IsCallerInRole ("Teller"), debe describir la funcionalidad a la que solo los cajeros tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="78ea6-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="78ea6-127">También debe especificar si un rol es necesario para ayudar a proteger el acceso a todo el componente.</span><span class="sxs-lookup"><span data-stu-id="78ea6-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78ea6-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78ea6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ea6-129">Autenticación de cliente</span><span class="sxs-lookup"><span data-stu-id="78ea6-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="78ea6-130">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="78ea6-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="78ea6-131">Seguridad de aplicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="78ea6-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="78ea6-132">Seguridad de aplicaciones de niveles múltiples</span><span class="sxs-lookup"><span data-stu-id="78ea6-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="78ea6-133">Administración de la seguridad basada en roles</span><span class="sxs-lookup"><span data-stu-id="78ea6-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="78ea6-134">Usar la Directiva de restricción de software en COM+</span><span class="sxs-lookup"><span data-stu-id="78ea6-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
