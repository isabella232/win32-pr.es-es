---
description: Descarga la firma del archivo. cab, comprueba los permisos asociados a los paquetes y los ejecuta según la autenticación.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660656"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="5cff2-103">DownloadJavaEX función)</span><span class="sxs-lookup"><span data-stu-id="5cff2-103">DownloadJavaEX function</span></span>

<span data-ttu-id="5cff2-104">Descarga la firma del archivo. cab, comprueba los permisos asociados a los paquetes y los ejecuta según la autenticación.</span><span class="sxs-lookup"><span data-stu-id="5cff2-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cff2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cff2-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="5cff2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cff2-107">*Reservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5cff2-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cff2-108">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="5cff2-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5cff2-109">*pProviderData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5cff2-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cff2-110">Una estructura de [**\_ \_ datos del proveedor de cifrado**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) que contiene los datos del certificado, como los permisos de archivo y de zona.</span><span class="sxs-lookup"><span data-stu-id="5cff2-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="5cff2-111">*pJava* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5cff2-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cff2-112">Estructura [**del \_ \_ proveedor de directivas de Java**](/previous-versions//bb432350(v=vs.85)) que contiene los datos relacionados con el proveedor de directivas.</span><span class="sxs-lookup"><span data-stu-id="5cff2-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="5cff2-113">*pFunctions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5cff2-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cff2-114">Una estructura de [**\_ \_ funciones de proveedor de cifrado**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) que contiene una lista de métodos para comprobar objetos de certificado, firmas y directivas finales.</span><span class="sxs-lookup"><span data-stu-id="5cff2-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="5cff2-115">*fCertificate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5cff2-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cff2-116">Si hay un certificado, este parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="5cff2-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="5cff2-117">De lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="5cff2-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5cff2-118">*pTrust* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5cff2-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cff2-119">Una estructura de [**\_ confianza de Java**](/windows/desktop/api/Capi/ns-capi-java_trust) que contiene información de confianza como el permiso codificado, la firma del codificador y el código de la Directiva de devolución auténtica.</span><span class="sxs-lookup"><span data-stu-id="5cff2-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cff2-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cff2-120">Return value</span></span>

<span data-ttu-id="5cff2-121">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5cff2-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="5cff2-122">De lo contrario, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="5cff2-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cff2-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cff2-123">Remarks</span></span>

<span data-ttu-id="5cff2-124">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5cff2-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cff2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cff2-125">Requirements</span></span>



| <span data-ttu-id="5cff2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cff2-126">Requirement</span></span> | <span data-ttu-id="5cff2-127">Value</span><span class="sxs-lookup"><span data-stu-id="5cff2-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cff2-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5cff2-128">DLL</span></span><br/> | <dl> <span data-ttu-id="5cff2-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cff2-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
