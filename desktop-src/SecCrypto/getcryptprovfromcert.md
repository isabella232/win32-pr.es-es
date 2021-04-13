---
description: Obtiene un identificador para un proveedor de servicios criptográficos (CSP) y una especificación de clave para un contexto de certificado.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361624"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="220cc-103">GetCryptProvFromCert función)</span><span class="sxs-lookup"><span data-stu-id="220cc-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="220cc-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="220cc-104">This API is deprecated.</span></span> <span data-ttu-id="220cc-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="220cc-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="220cc-106">La función **GetCryptProvFromCert** obtiene un identificador a un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y una especificación de clave para un contexto de [*certificado*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="220cc-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="220cc-107">Utilice esta función para obtener acceso a la [*clave privada*](../secgloss/p-gly.md) del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="220cc-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="220cc-108">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="220cc-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="220cc-109">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="220cc-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="220cc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="220cc-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="220cc-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="220cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220cc-112">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="220cc-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-113">Identificador de la ventana que se va a usar como propietario de los cuadros de diálogo que se muestran.</span><span class="sxs-lookup"><span data-stu-id="220cc-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="220cc-114">Este miembro no se utiliza actualmente y se omite.</span><span class="sxs-lookup"><span data-stu-id="220cc-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="220cc-115">Es seguro pasar **null** para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="220cc-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-116">*pCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="220cc-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-117">Puntero a una estructura [**de \_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para el certificado.</span><span class="sxs-lookup"><span data-stu-id="220cc-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-118">*phCryptProv* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="220cc-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-119">Puntero a una estructura [**HCRYPTPROV**](hcryptprov.md) que es un identificador para el CSP.</span><span class="sxs-lookup"><span data-stu-id="220cc-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-120">*pdwKeySpec* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="220cc-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-121">Especificación de la clave privada que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="220cc-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="220cc-122">Entre los valores posibles se incluyen **en \_ KEYEXCHANGE** o **en la \_ signatura**.</span><span class="sxs-lookup"><span data-stu-id="220cc-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-123">*pfDidCryptAcquire* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="220cc-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-124">Valor que especifica si la función adquirió el identificador del proveedor basándose en el certificado.</span><span class="sxs-lookup"><span data-stu-id="220cc-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-125">*ppwszTmpContainer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="220cc-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-126">Dirección de un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal.</span><span class="sxs-lookup"><span data-stu-id="220cc-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="220cc-127">La función **GetCryptProvFromCert** proporciona e inicializa el contenedor temporal.</span><span class="sxs-lookup"><span data-stu-id="220cc-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="220cc-128">Al llamar a **GetCryptProvFromCert**, la dirección debe apuntar a un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="220cc-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-129">*ppwszProviderName* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="220cc-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-130">Dirección de un puntero a una cadena terminada en null para el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="220cc-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="220cc-131">La función **GetCryptProvFromCert** devuelve el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="220cc-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="220cc-132">Al llamar a **GetCryptProvFromCert**, la dirección debe apuntar a un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="220cc-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="220cc-133">*pdwProviderType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="220cc-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="220cc-134">Especifica el tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="220cc-134">Specifies the CSP type.</span></span> <span data-ttu-id="220cc-135">Puede ser cero o uno de los [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="220cc-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="220cc-136">Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.</span><span class="sxs-lookup"><span data-stu-id="220cc-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220cc-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="220cc-137">Return value</span></span>

<span data-ttu-id="220cc-138">Cuando se realiza correctamente, esta función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="220cc-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="220cc-139">La función **GetCryptProvFromCert** devuelve **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="220cc-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="220cc-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="220cc-140">Remarks</span></span>

<span data-ttu-id="220cc-141">La herramienta [Makecert](makecert.md) llama a **GetCryptProvFromCert** cuando se invoca mediante la opción **de línea de comandos-is** .</span><span class="sxs-lookup"><span data-stu-id="220cc-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="220cc-142">Si el parámetro *pfDidCryptAcquire* se establece en **true**, la función establece los parámetros *phCryptProv*, *pdwKeySpec* y *pdwProviderType* en los valores del proveedor.</span><span class="sxs-lookup"><span data-stu-id="220cc-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="220cc-143">Cuando haya terminado de usar el CSP, libere el servicio llamando a la función [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="220cc-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="220cc-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="220cc-144">Requirements</span></span>



| <span data-ttu-id="220cc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="220cc-145">Requirement</span></span> | <span data-ttu-id="220cc-146">Value</span><span class="sxs-lookup"><span data-stu-id="220cc-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="220cc-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="220cc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="220cc-148">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="220cc-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="220cc-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="220cc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="220cc-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="220cc-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="220cc-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="220cc-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="220cc-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="220cc-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
