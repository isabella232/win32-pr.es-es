---
title: Enlazar con ADsOpenObject y IADsOpenDSObject OpenDSObject
description: La función ADsOpenObject y el método IADsOpenDSObject OpenDSObject se usan para enlazar con objetos de servicio de directorio cuando se deben especificar credenciales alternativas y cuando se requiere el cifrado de datos.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Enlazar con ADsOpenObject y IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI, usar, enlazar con ADsOpenObject y IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078362"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="50fdf-105">Enlazar con ADsOpenObject y IADsOpenDSObject:: OpenDSObject</span><span class="sxs-lookup"><span data-stu-id="50fdf-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="50fdf-106">La función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) se usan para enlazar con objetos de servicio de directorio cuando se deben especificar credenciales alternativas y cuando se requiere el cifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="50fdf-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="50fdf-107">Las credenciales del subproceso que realiza la llamada deben usarse cuando sea posible.</span><span class="sxs-lookup"><span data-stu-id="50fdf-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="50fdf-108">Sin embargo, si se deben usar credenciales alternativas, se debe usar la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="50fdf-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="50fdf-109">Si se usan credenciales alternativas, es importante no almacenar en caché la contraseña.</span><span class="sxs-lookup"><span data-stu-id="50fdf-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="50fdf-110">Se pueden realizar varias operaciones de enlace especificando el nombre de usuario y la contraseña para la primera operación de enlace y, a continuación, especificando solo el nombre de usuario en los enlaces subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="50fdf-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="50fdf-111">El sistema configura una sesión en la primera llamada y usa la misma sesión en las llamadas de enlace subsiguientes siempre que se cumplan las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="50fdf-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="50fdf-112">El mismo nombre de usuario en cada operación de enlace.</span><span class="sxs-lookup"><span data-stu-id="50fdf-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="50fdf-113">Implemente el enlace sin servidor o enlace al mismo servidor en cada operación de enlace.</span><span class="sxs-lookup"><span data-stu-id="50fdf-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="50fdf-114">Mantenga una sesión abierta manteniendo en una referencia de objeto de una de las operaciones de enlace.</span><span class="sxs-lookup"><span data-stu-id="50fdf-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="50fdf-115">La sesión se cierra cuando se libera la última referencia de objeto.</span><span class="sxs-lookup"><span data-stu-id="50fdf-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="50fdf-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) usan las interfaces del [proveedor de compatibilidad para seguridad (SSPI)](/windows/desktop/SecAuthN/sspi) de Windows NT para ofrecer flexibilidad en las opciones de autenticación.</span><span class="sxs-lookup"><span data-stu-id="50fdf-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="50fdf-117">La principal ventaja de utilizar estas interfaces es proporcionar diferentes tipos de autenticación a Active Directory clientes y cifrar la sesión.</span><span class="sxs-lookup"><span data-stu-id="50fdf-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="50fdf-118">Actualmente, ADSI no permite que se pasen los certificados.</span><span class="sxs-lookup"><span data-stu-id="50fdf-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="50fdf-119">Por lo tanto, puede usar SSL para el cifrado y, después, Kerberos, NTLM o autenticación simple, en función de cómo se establezcan las marcas en el parámetro *dwReserved* .</span><span class="sxs-lookup"><span data-stu-id="50fdf-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="50fdf-120">No se puede solicitar un proveedor de SSPI específico en ADSI, aunque siempre se obtiene el protocolo de preferencias más alto.</span><span class="sxs-lookup"><span data-stu-id="50fdf-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="50fdf-121">En el caso de un cliente de Windows que se enlaza a un equipo que ejecuta Windows, el protocolo es Kerberos.</span><span class="sxs-lookup"><span data-stu-id="50fdf-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="50fdf-122">No permitir un certificado para la autenticación es aceptable en el caso de una página web porque la autenticación se produce antes de ejecutar la Página Web.</span><span class="sxs-lookup"><span data-stu-id="50fdf-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="50fdf-123">Aunque las operaciones de apertura permiten especificar un usuario y una contraseña, no debe hacerlo.</span><span class="sxs-lookup"><span data-stu-id="50fdf-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="50fdf-124">En su lugar, no especifique ninguna credencial y use implícitamente las credenciales del contexto de seguridad del llamador.</span><span class="sxs-lookup"><span data-stu-id="50fdf-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="50fdf-125">Para enlazar a un objeto de directorio con las credenciales del autor de la llamada con [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), especifique **null** para el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="50fdf-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="50fdf-126">Por último, para enlazar sin autenticación, use la marca **ADS \_ no \_ Authentication** .</span><span class="sxs-lookup"><span data-stu-id="50fdf-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="50fdf-127">Sin autenticación indica que ADSI intenta enlazar como un usuario anónimo al objeto de destino y no realiza ninguna autenticación.</span><span class="sxs-lookup"><span data-stu-id="50fdf-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="50fdf-128">Esto es equivalente a solicitar un enlace anónimo en LDAP e indica que todos los usuarios están incluidos en el contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="50fdf-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="50fdf-129">Si las marcas de autenticación se establecen en cero, ADSI realiza un enlace simple, enviado como texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="50fdf-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="50fdf-130">Si se especifica un nombre de usuario y una contraseña sin especificar marcas de autenticación, el nombre de usuario y la contraseña se transmiten por la red en texto sin formato, lo que constituye un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="50fdf-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="50fdf-131">No especifique un nombre de usuario y una contraseña sin especificar marcas de autenticación.</span><span class="sxs-lookup"><span data-stu-id="50fdf-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="50fdf-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50fdf-132">Examples</span></span>

<span data-ttu-id="50fdf-133">En el siguiente ejemplo de código de Visual Basic se muestra cómo usar el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="50fdf-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="50fdf-134">En el ejemplo de código de C++ siguiente se muestra cómo usar la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="50fdf-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



<span data-ttu-id="50fdf-135">La interfaz [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) también se puede usar en C++, pero duplica la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="50fdf-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="50fdf-136">En el ejemplo de código de C++ siguiente se muestra cómo utilizar la interfaz [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) para realizar la misma operación de enlace que en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="50fdf-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 