---
title: Enlazar con GetObject y ADsGetObject
description: Las funciones GetObject y ADsGetObject se usan para enlazar con objetos de servicio de directorio sin autenticación.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, enlazar con GetObject y ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995616"
---
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="417bb-104">Enlazar con GetObject y ADsGetObject</span><span class="sxs-lookup"><span data-stu-id="417bb-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="417bb-105">Las funciones **GetObject** y [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) se usan para enlazar con objetos de servicio de directorio sin autenticación.</span><span class="sxs-lookup"><span data-stu-id="417bb-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="417bb-106">No es necesario que la aplicación proporcione credenciales al acceder a los datos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="417bb-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="417bb-107">ADSI utiliza el contexto de seguridad del subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="417bb-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="417bb-108">Sin embargo, si se produce un error en la autenticación segura, ADSI intenta realizar un enlace simple con un nombre de usuario NULL y una contraseña nula.</span><span class="sxs-lookup"><span data-stu-id="417bb-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="417bb-109">Si el enlace simple se realiza correctamente, el contexto de usuario para el enlace es Guest.</span><span class="sxs-lookup"><span data-stu-id="417bb-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="417bb-110">Un enlace simple utiliza la autenticación de texto simple.</span><span class="sxs-lookup"><span data-stu-id="417bb-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="417bb-111">Dado que no se transmite ningún nombre de usuario o contraseña a través de la red, no se trata de un problema de seguridad.</span><span class="sxs-lookup"><span data-stu-id="417bb-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="417bb-112">La función **GetObject** se utiliza para enlazar con objetos de servicio de directorio en lenguajes que admiten la automatización, como Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="417bb-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="417bb-113">La función **GetObject** requiere una cadena de moniker.</span><span class="sxs-lookup"><span data-stu-id="417bb-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="417bb-114">En ADSI, la cadena de enlace es la cadena de moniker.</span><span class="sxs-lookup"><span data-stu-id="417bb-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="417bb-115">En los lenguajes que no admiten directamente automatización, como C o C++, ADSI proporciona la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para enlazar con objetos de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="417bb-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="417bb-116">Como alternativa, las funciones [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) y [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) se pueden usar para lograr el mismo resultado que **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="417bb-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="417bb-117">Para un servicio que se ejecuta con la cuenta LocalSystem, el contexto de seguridad utilizado por **GetObject** y [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depende del equipo en el que se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="417bb-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="417bb-118">Si el servicio se ejecuta como LocalSystem en un controlador de dominio, el servicio tiene acceso de nivel de sistema completo a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="417bb-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="417bb-119">Si el servicio no se está ejecutando en un controlador de dominio, el servicio tiene los derechos de acceso y los privilegios concedidos a la cuenta de equipo para el equipo en el que se está ejecutando el servicio; Esto es significativamente menos eficaz que el acceso de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="417bb-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="417bb-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="417bb-120">Examples</span></span>

<span data-ttu-id="417bb-121">En el siguiente ejemplo de código de Visual Basic se muestra cómo utilizar la función **GetObject** para enlazar a un objeto.</span><span class="sxs-lookup"><span data-stu-id="417bb-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="417bb-122">En el ejemplo de código de C++ siguiente se muestra cómo usar la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para enlazar a un objeto.</span><span class="sxs-lookup"><span data-stu-id="417bb-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 