---
description: Devuelve las credenciales para autenticar un contenedor que no está unido a un dominio con Active Directory.
title: Método ICcgDomainAuthCredentials::GetPasswordCredentials (ccgplugins.h)
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387828"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="3a004-103">ICcgDomainAuthCredentials::GetPasswordCredentials (método)</span><span class="sxs-lookup"><span data-stu-id="3a004-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="3a004-104">Devuelve las credenciales para autenticar un contenedor que no está unido a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3a004-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a004-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a004-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="3a004-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a004-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a004-107">*pluginInput* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3a004-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a004-108">Cadena de entrada pasada por el entorno de ejecución del contenedor.</span><span class="sxs-lookup"><span data-stu-id="3a004-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="3a004-109">La implementación del cliente usa la cadena de entrada proporcionada para recuperar las credenciales de autenticación, normalmente de un proveedor de almacenamiento seguro, que se devuelven en los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="3a004-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="3a004-110">La cadena de entrada se proporciona al host Compute Services (HCS) en un archivo de especificación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="3a004-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="3a004-111">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="3a004-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3a004-112">*domainName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a004-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a004-113">Nombre de dominio de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="3a004-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3a004-114">*nombre de usuario* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a004-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a004-115">Nombre de usuario de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="3a004-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3a004-116">*contraseña* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a004-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a004-117">Contraseña de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="3a004-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a004-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a004-118">Return value</span></span>

<span data-ttu-id="3a004-119">El valor devuelto es **un HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3a004-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="3a004-120">Un valor de S \_ OK indica que la llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a004-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a004-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a004-121">Remarks</span></span>

<span data-ttu-id="3a004-122">Se puede llamar a la API simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="3a004-122">The API may be called concurrently.</span></span> <span data-ttu-id="3a004-123">Por lo tanto, el desarrollador debe asegurarse de que su implementación es segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3a004-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="3a004-124">Además, el objeto COM se activará fuera de proceso y se debe registrar correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a004-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="3a004-125">El implementador debe agregar una clave en "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" para su CLSID COM.</span><span class="sxs-lookup"><span data-stu-id="3a004-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="3a004-126">El acceso de escritura a "CCG\COMClasses" está restringido a las cuentas SYSTEM y Administrator.</span><span class="sxs-lookup"><span data-stu-id="3a004-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="3a004-127">A continuación se muestra un archivo de especificación de credenciales de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3a004-127">The following is an example credential specification file.</span></span> <span data-ttu-id="3a004-128">Para obtener información sobre cómo proporcionar este archivo a Docker, [consulte Ejecución de un contenedor con una gMSA.](/virtualization/windowscontainers/manage-containers/gmsa-run-container)</span><span class="sxs-lookup"><span data-stu-id="3a004-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="3a004-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3a004-129">Examples</span></span>

<span data-ttu-id="3a004-130">En el ejemplo siguiente se muestra una implementación sencilla de **ICcgDomainAuthCredentials**.</span><span class="sxs-lookup"><span data-stu-id="3a004-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="3a004-131">Tenga en cuenta que, para fines ilustrativos, este ejemplo obtiene las credenciales simplemente analizando la cadena de entrada.</span><span class="sxs-lookup"><span data-stu-id="3a004-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="3a004-132">Una implementación real almacenaría las credenciales en un almacén de datos seguro y usaría la cadena de entrada para localizar la información de credenciales.</span><span class="sxs-lookup"><span data-stu-id="3a004-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="3a004-133">Además, las implementaciones del método COM estándar se han omitido en este ejemplo por brevedad.</span><span class="sxs-lookup"><span data-stu-id="3a004-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="3a004-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a004-134">Requirements</span></span>




| <span data-ttu-id="3a004-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a004-135">Requirement</span></span> | <span data-ttu-id="3a004-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3a004-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a004-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a004-137">Minimum supported server</span></span> | <span data-ttu-id="3a004-138">Windows Server, versión 2004</span><span class="sxs-lookup"><span data-stu-id="3a004-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="3a004-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a004-139">Header</span></span>                   | <span data-ttu-id="3a004-140">ccgplugins.h</span><span class="sxs-lookup"><span data-stu-id="3a004-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="3a004-141">IID</span><span class="sxs-lookup"><span data-stu-id="3a004-141">IID</span></span>                    | <span data-ttu-id="3a004-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="3a004-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

