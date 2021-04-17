---
description: Lo utiliza un proveedor de servicios criptográficos (CSP) para comprobar la firma de un archivo DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE puntero a función (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687598"
---
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="d72cb-103">CIFRAr \_ comprobar \_ puntero de función de imagen</span><span class="sxs-lookup"><span data-stu-id="d72cb-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="d72cb-104">Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utiliza la función de devolución de llamada **FuncVerifyImage** para comprobar la firma de un archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d72cb-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="d72cb-105">Todas las DLL auxiliares en las que un CSP realiza llamadas a funciones deben estar firmadas de la misma manera (y con la misma clave) que la DLL de CSP principal.</span><span class="sxs-lookup"><span data-stu-id="d72cb-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="d72cb-106">Para garantizar esta firma, los archivos dll auxiliares se deben cargar dinámicamente mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="d72cb-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="d72cb-107">Pero antes de que se cargue el archivo DLL, se debe comprobar la firma de la DLL.</span><span class="sxs-lookup"><span data-stu-id="d72cb-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="d72cb-108">El CSP realiza esta comprobación mediante una llamada a la función **FuncVerifyImage** , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d72cb-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="d72cb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d72cb-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="d72cb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d72cb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72cb-111">*lpszImage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d72cb-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d72cb-112">Dirección de una cadena terminada en null que contiene la ruta de acceso y el nombre de archivo del archivo DLL para el que se va a comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="d72cb-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="d72cb-113">*pbSigData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d72cb-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d72cb-114">Dirección de un búfer que contiene la firma.</span><span class="sxs-lookup"><span data-stu-id="d72cb-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72cb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d72cb-115">Return value</span></span>

<span data-ttu-id="d72cb-116">Devuelve **true** si la función se ejecuta correctamente, **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d72cb-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="d72cb-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d72cb-117">Examples</span></span>

<span data-ttu-id="d72cb-118">En el ejemplo siguiente se muestra cómo usar la función de devolución de llamada **FuncVerifyImage** para comprobar la firma de un archivo dll antes de que lo cargue un CSP.</span><span class="sxs-lookup"><span data-stu-id="d72cb-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a><span data-ttu-id="d72cb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d72cb-119">Requirements</span></span>



| <span data-ttu-id="d72cb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d72cb-120">Requirement</span></span> | <span data-ttu-id="d72cb-121">Value</span><span class="sxs-lookup"><span data-stu-id="d72cb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d72cb-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d72cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d72cb-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d72cb-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d72cb-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d72cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d72cb-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d72cb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d72cb-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d72cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d72cb-127"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d72cb-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d72cb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d72cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72cb-129">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="d72cb-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="d72cb-130">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="d72cb-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
