---
title: Compatibilidad con enlaces tempranas
description: En el ejemplo de código siguiente se presenta un escenario con compatibilidad de enlace temprana en contexto.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, compatibilidad con enlaces tempranas
- enlace de AD, compatibilidad con enlaces tempranas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149623"
---
# <a name="early-binding-support"></a><span data-ttu-id="df9ba-105">Compatibilidad con enlaces tempranas</span><span class="sxs-lookup"><span data-stu-id="df9ba-105">Early Binding Support</span></span>

<span data-ttu-id="df9ba-106">En el ejemplo de código siguiente se presenta un escenario con compatibilidad de enlace temprana en contexto.</span><span class="sxs-lookup"><span data-stu-id="df9ba-106">The following code example presents a scenario with early binding support in place.</span></span>


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



<span data-ttu-id="df9ba-107">En este ejemplo de código, dos componentes de extensión extienden un objeto de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="df9ba-107">In this code example, two extension components extend a **user** object.</span></span> <span data-ttu-id="df9ba-108">Cada extensión publica su propia interfaz.</span><span class="sxs-lookup"><span data-stu-id="df9ba-108">Each extension publishes its own interface.</span></span> <span data-ttu-id="df9ba-109">Cada extensión no reconoce la otra interfaz de extensión; solo ADSI reconoce la existencia de ambas extensiones.</span><span class="sxs-lookup"><span data-stu-id="df9ba-109">Each extension does not recognize the other extension interface; only ADSI recognizes the existence of both extensions.</span></span> <span data-ttu-id="df9ba-110">Cada extensión delega su [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en ADSI.</span><span class="sxs-lookup"><span data-stu-id="df9ba-110">Each extension delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to ADSI.</span></span> <span data-ttu-id="df9ba-111">ADSI actúa como agregador para ambas extensiones y para cualquier otra extensión futura.</span><span class="sxs-lookup"><span data-stu-id="df9ba-111">ADSI acts as an aggregator for both extensions, and any other future extensions.</span></span> <span data-ttu-id="df9ba-112">Al consultar una interfaz desde cualquier extensión o desde ADSI, se produce el mismo resultado coherente.</span><span class="sxs-lookup"><span data-stu-id="df9ba-112">Querying an interface from any extension, or from ADSI, yields the same consistent result.</span></span>

<span data-ttu-id="df9ba-113">En el procedimiento siguiente se describe cómo crear una extensión.</span><span class="sxs-lookup"><span data-stu-id="df9ba-113">The following procedure describes how to create an extension.</span></span>

## <a name="step-1-add-aggregation-to-your-component"></a><span data-ttu-id="df9ba-114">Paso 1: agregar agregación al componente</span><span class="sxs-lookup"><span data-stu-id="df9ba-114">Step 1: Add Aggregation to Your Component</span></span>

<span data-ttu-id="df9ba-115">Siga la especificación COM para agregar agregaciones al componente.</span><span class="sxs-lookup"><span data-stu-id="df9ba-115">Follow the COM specification for adding aggregation to your component.</span></span> <span data-ttu-id="df9ba-116">En Resumen, debe aceptar las solicitudes *pUnknown* para el componente durante **CreateInstance** y delegar el *pUnknown* en el [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del agregador si se agrega el componente.</span><span class="sxs-lookup"><span data-stu-id="df9ba-116">In summary, you must accept the *pUnknown* requests to your component during **CreateInstance**, and delegate the *pUnknown* to the aggregator's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) if the component is aggregated.</span></span>

## <a name="step-2-register-your-extension"></a><span data-ttu-id="df9ba-117">Paso 2: registrar la extensión</span><span class="sxs-lookup"><span data-stu-id="df9ba-117">Step 2: Register Your Extension</span></span>

<span data-ttu-id="df9ba-118">Ahora debe decidir qué clase de directorio se va a extender.</span><span class="sxs-lookup"><span data-stu-id="df9ba-118">Now you must decide which directory class to extend.</span></span> <span data-ttu-id="df9ba-119">No se pueden usar las mismas interfaces para lograr esto que se usaría para una interfaz ADSI, por ejemplo, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="df9ba-119">You cannot use the same interfaces to accomplish this that you would use for an ADSI interface, for example, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span></span> <span data-ttu-id="df9ba-120">Los objetos de directorio se conservan en el directorio, mientras que la extensión y ADSI se ejecutan en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="df9ba-120">Directory objects are persisted in the directory, while your extension and ADSI are running on the client computer.</span></span> <span data-ttu-id="df9ba-121">Los ejemplos de objetos de directorio son **User**, **Computer**, **printQueue**, **serviceConnectionPoint** y **nTDSService**.</span><span class="sxs-lookup"><span data-stu-id="df9ba-121">Directory object examples are **user**, **computer**, **printQueue**, **serviceConnectionPoint**, and **nTDSService**.</span></span> <span data-ttu-id="df9ba-122">También puede Agregar una nueva clase en Active Directory y crear una nueva extensión para esta nueva clase.</span><span class="sxs-lookup"><span data-stu-id="df9ba-122">You can add a new class in Active Directory and create a new extension for this new class as well.</span></span>

<span data-ttu-id="df9ba-123">Utilice las claves del registro para asociar un nombre de clase de directorio a los componentes de extensión ADSI.</span><span class="sxs-lookup"><span data-stu-id="df9ba-123">You use registry keys to associate a directory class name with the ADSI extension components.</span></span> <span data-ttu-id="df9ba-124">En la ilustración siguiente se representa el diseño del registro existente, así como las nuevas claves.</span><span class="sxs-lookup"><span data-stu-id="df9ba-124">The following figure represents the existing registry layout, as a well as new keys.</span></span>

-   <span data-ttu-id="df9ba-125">Una nueva clave, denominada **extensions**, contiene una lista de claves, cada una de las cuales representa una clase en el directorio.</span><span class="sxs-lookup"><span data-stu-id="df9ba-125">A new key, called **Extensions**, contains a list of keys, each of which represents a class in the directory.</span></span> <span data-ttu-id="df9ba-126">Cada clase, por ejemplo, **usuario**, **printQueue** o **equipo**, mantiene una lista de subclaves.</span><span class="sxs-lookup"><span data-stu-id="df9ba-126">Each class, for example, **user**, **printQueue**, or **computer**, maintains a list of subkeys.</span></span>
-   <span data-ttu-id="df9ba-127">Cada subclave contiene el CLSID del componente de extensión ADSI.</span><span class="sxs-lookup"><span data-stu-id="df9ba-127">Each subkey contains the CLSID of the ADSI extension component.</span></span>
-   <span data-ttu-id="df9ba-128">Cada subclave CLSID contiene una entrada de cadena que permite varios valores.</span><span class="sxs-lookup"><span data-stu-id="df9ba-128">Each CLSID subkey contains a string entry that allows multiple values.</span></span> <span data-ttu-id="df9ba-129">Solo debe enumerar las interfaces que participan en la agregación.</span><span class="sxs-lookup"><span data-stu-id="df9ba-129">You should only list the interfaces that participate in the aggregation.</span></span>

> [!Note]  
> <span data-ttu-id="df9ba-130">Los objetos de extensión siguen siendo necesarios para registrar las claves COM estándar.</span><span class="sxs-lookup"><span data-stu-id="df9ba-130">Extension objects are still required to register standard COM keys.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a><span data-ttu-id="df9ba-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df9ba-131">Example</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

<span data-ttu-id="df9ba-132">La lista de interfaces de Extension1 puede ser diferente de la de Extension2.</span><span class="sxs-lookup"><span data-stu-id="df9ba-132">The list of interfaces from Extension1 can be different from that of Extension2.</span></span> <span data-ttu-id="df9ba-133">El objeto, cuando está activo, admite las interfaces del agregador (ADSI) y todas las interfaces proporcionadas por los Extension1 y Extension2 del agregado.</span><span class="sxs-lookup"><span data-stu-id="df9ba-133">The object, when active, supports the interfaces of the aggregator (ADSI) and all the interfaces provided by the aggregate's Extension1 and Extension2.</span></span> <span data-ttu-id="df9ba-134">La resolución de interfaces conflictivas (la misma interfaz que admiten tanto el agregador como los agregados o mediante varios agregados) se determina mediante prioridades de las extensiones.</span><span class="sxs-lookup"><span data-stu-id="df9ba-134">Resolution of conflicting interfaces (the same interface supported by both the aggregator and the aggregates or by multiple aggregates) is determined by priorities of the extensions.</span></span>

<span data-ttu-id="df9ba-135">También puede asociar la extensión CLSID con varios nombres de clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="df9ba-135">You can also associate your CLSID extension with multiple object class names.</span></span> <span data-ttu-id="df9ba-136">Por ejemplo, la extensión puede extender los objetos **User** y **Contact** .</span><span class="sxs-lookup"><span data-stu-id="df9ba-136">For example, your extension can extend both the **user** and **contact** objects.</span></span>

> [!Note]  
> <span data-ttu-id="df9ba-137">El comportamiento de la extensión se agrega en una clase por objeto, no en una instancia por objeto.</span><span class="sxs-lookup"><span data-stu-id="df9ba-137">Extension behavior is added on a per-object class, not on a per-object instance.</span></span>

 

<span data-ttu-id="df9ba-138">Como procedimiento recomendado, registre las extensiones, como haría con cualquier otro componente COM, con una llamada a la función **DllRegisterSvr** .</span><span class="sxs-lookup"><span data-stu-id="df9ba-138">As a best practice, register your extensions, as you would any other COM components, with a call to the **DllRegisterSvr** function.</span></span> <span data-ttu-id="df9ba-139">Proporcione también una utilidad para anular el registro de la extensión con la función **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="df9ba-139">Also provide a facility to unregister your extension with the **DllUnregisterServer** function.</span></span>

<span data-ttu-id="df9ba-140">En el ejemplo de código siguiente se muestra cómo registrar una extensión.</span><span class="sxs-lookup"><span data-stu-id="df9ba-140">The following code example shows how to register an extension.</span></span>


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 