---
title: Uso de un moniker de sesión
description: La activación de sesión a sesión permite que un proceso de cliente Active un proceso de servidor local en una sesión especificada.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359323"
---
# <a name="using-a-session-moniker"></a><span data-ttu-id="2f470-103">Uso de un moniker de sesión</span><span class="sxs-lookup"><span data-stu-id="2f470-103">Using a Session Moniker</span></span>

<span data-ttu-id="2f470-104">La activación de sesión a sesión permite que un proceso de cliente Active un proceso de servidor local en una sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="2f470-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="2f470-105">Puede hacerlo por sesión mediante un moniker de sesión proporcionado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="2f470-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="2f470-106">Para obtener más información sobre cómo crear un moniker de sesión, consulte [activación de sesión en sesión con un moniker](session-to-session-activation-with-a-session-moniker.md)de sesión.</span><span class="sxs-lookup"><span data-stu-id="2f470-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="2f470-107">En el ejemplo siguiente se muestra cómo activar un proceso de servidor local con el ID. de clase "10000013-0000-0000-0000-000000000001" en la sesión con el identificador de sesión 3.</span><span class="sxs-lookup"><span data-stu-id="2f470-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="2f470-108">En primer lugar, el ejemplo llama a la función [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="2f470-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="2f470-109">Después, el ejemplo llama a [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) para recuperar un puntero a una implementación de la interfaz [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="2f470-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="2f470-110">Este objeto almacena información sobre las operaciones de enlace de moniker; el puntero es necesario para llamar a los métodos de la interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="2f470-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="2f470-111">A continuación, el ejemplo llama a la función [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) para crear el moniker de sesión compuesto y, a continuación, el método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para activar la conexión entre el cliente y el proceso de servidor, mediante el moniker de sesión recién creado.</span><span class="sxs-lookup"><span data-stu-id="2f470-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="2f470-112">En este momento puede usar el puntero de interfaz para realizar las operaciones deseadas en el objeto.</span><span class="sxs-lookup"><span data-stu-id="2f470-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="2f470-113">Finalmente, el ejemplo libera el contexto de enlace y llama a la función [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="2f470-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



<span data-ttu-id="2f470-114">Como "{ID. de clase de la clase moniker}" es también una forma de asignar un nombre a un moniker de clase, puede usar la cadena siguiente para asignar un nombre al moniker compuesto (el moniker de la sesión compuesto por el moniker de la clase) en lugar de la forma que se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2f470-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="2f470-115">Si el mismo usuario ha iniciado sesión en cada sesión durante una activación entre sesiones, puede activar correctamente cualquier proceso de servidor configurado para ejecutarse en el modo de activación de usuario interactivo de runas.</span><span class="sxs-lookup"><span data-stu-id="2f470-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="2f470-116">Si varios usuarios inician sesión en cada sesión, el servidor debe llamar a la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer los derechos de usuario adecuados antes de que se pueda realizar una activación y una conexión correctas entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="2f470-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="2f470-117">Una manera de lograr esto sería que el servidor implementara una interfaz [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizada y pasara la implementación a **CoInitializeSecurity**.</span><span class="sxs-lookup"><span data-stu-id="2f470-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="2f470-118">En cualquier caso, el usuario del cliente debe tener los permisos de [**Inicio**](../com/launchpermission.md) y [**acceso**](../com/accesspermission.md) adecuados especificados por la aplicación que se ejecuta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2f470-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="2f470-119">Para obtener más información, vea [seguridad en com](../com/security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="2f470-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="2f470-120">Para obtener más información acerca de los monikers y los monikers proporcionados por el sistema y los modos de activación, consulte [monikers](../com/monikers.md), la interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) y la [clave AppID](/windows/desktop/com/appid-key) en la documentación de com del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="2f470-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 