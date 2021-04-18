---
description: Devuelve las credenciales para autenticar un contenedor no unido a un dominio con Active Directory.
title: 'ICcgDomainAuthCredentials:: GetPasswordCredentials (método) (ccgplugins. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721597"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="ffe98-103">ICcgDomainAuthCredentials:: GetPasswordCredentials (método)</span><span class="sxs-lookup"><span data-stu-id="ffe98-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="ffe98-104">Devuelve las credenciales para autenticar un contenedor no unido a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ffe98-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe98-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffe98-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="ffe98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffe98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe98-107">*pluginInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ffe98-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe98-108">Una cadena de entrada pasada por el tiempo de ejecución del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffe98-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="ffe98-109">La implementación del cliente utiliza la cadena de entrada proporcionada para recuperar las credenciales de autenticación, normalmente de un proveedor de almacenamiento seguro, que se devuelven en los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="ffe98-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="ffe98-110">La cadena de entrada se proporciona al Compute Services Host (HCS) en un archivo de especificación de credenciales.</span><span class="sxs-lookup"><span data-stu-id="ffe98-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="ffe98-111">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="ffe98-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ffe98-112">*dominio* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ffe98-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe98-113">El nombre de dominio para las credenciales.</span><span class="sxs-lookup"><span data-stu-id="ffe98-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ffe98-114">*nombre de usuario* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ffe98-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe98-115">El nombre de usuario de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="ffe98-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ffe98-116">*contraseña* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ffe98-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe98-117">Contraseña de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="ffe98-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe98-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffe98-118">Return value</span></span>

<span data-ttu-id="ffe98-119">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ffe98-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="ffe98-120">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ffe98-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe98-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffe98-121">Remarks</span></span>

<span data-ttu-id="ffe98-122">Se puede llamar a la API simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="ffe98-122">The API may be called concurrently.</span></span> <span data-ttu-id="ffe98-123">Por lo tanto, el desarrollador debe asegurarse de que su implementación sea segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ffe98-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="ffe98-124">Además, el objeto COM se activará fuera del proceso y debe registrarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="ffe98-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="ffe98-125">El implementador debe agregar una clave en "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" para su CLSID COM.</span><span class="sxs-lookup"><span data-stu-id="ffe98-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="ffe98-126">El acceso de escritura a "CCG\COMClasses" está restringido a las cuentas de sistema y de administrador.</span><span class="sxs-lookup"><span data-stu-id="ffe98-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="ffe98-127">El siguiente es un archivo de especificación de credenciales de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ffe98-127">The following is an example credential specification file.</span></span> <span data-ttu-id="ffe98-128">Para obtener información sobre cómo proporcionar este archivo a Docker, consulte [ejecución de un contenedor con un gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span><span class="sxs-lookup"><span data-stu-id="ffe98-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

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

## <a name="examples"></a><span data-ttu-id="ffe98-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ffe98-129">Examples</span></span>

<span data-ttu-id="ffe98-130">En el ejemplo siguiente se muestra una implementación sencilla de **ICcgDomainAuthCredentials**.</span><span class="sxs-lookup"><span data-stu-id="ffe98-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="ffe98-131">Tenga en cuenta que, con fines ilustrativos, este ejemplo obtiene las credenciales simplemente analizando la cadena de entrada.</span><span class="sxs-lookup"><span data-stu-id="ffe98-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="ffe98-132">Una implementación del mundo real almacenaría las credenciales en un almacén de datos seguro y utilizaría la cadena de entrada para buscar la información de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="ffe98-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="ffe98-133">Además, las implementaciones de método COM estándar se han omitido en este ejemplo por motivos de brevedad.</span><span class="sxs-lookup"><span data-stu-id="ffe98-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ffe98-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffe98-134">Requirements</span></span>




| <span data-ttu-id="ffe98-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffe98-135">Requirement</span></span> | <span data-ttu-id="ffe98-136">Value</span><span class="sxs-lookup"><span data-stu-id="ffe98-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe98-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffe98-137">Minimum supported server</span></span> | <span data-ttu-id="ffe98-138">Windows Server, versión 2004</span><span class="sxs-lookup"><span data-stu-id="ffe98-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="ffe98-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffe98-139">Header</span></span>                   | <span data-ttu-id="ffe98-140">ccgplugins. h</span><span class="sxs-lookup"><span data-stu-id="ffe98-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="ffe98-141">IID</span><span class="sxs-lookup"><span data-stu-id="ffe98-141">IID</span></span>                    | <span data-ttu-id="ffe98-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="ffe98-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

