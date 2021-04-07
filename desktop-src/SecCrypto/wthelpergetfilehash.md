---
description: Comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002077"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="5f8aa-103">WTHelperGetFileHash función)</span><span class="sxs-lookup"><span data-stu-id="5f8aa-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="5f8aa-104">\[La función **WTHelperGetFileHash** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f8aa-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5f8aa-106">La función **WTHelperGetFileHash** comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="5f8aa-107">Esta función no se declara en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="5f8aa-108">Para usar esta función, declárela en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="5f8aa-109">Esta función tampoco tiene asociada ninguna biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-109">This function also has no associated import library.</span></span> <span data-ttu-id="5f8aa-110">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5f8aa-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f8aa-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="5f8aa-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f8aa-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8aa-113">*pwszFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8aa-114">Puntero a una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre del archivo para el que se va a obtener el hash.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="5f8aa-115">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8aa-116">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f8aa-117">*pvReserved* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8aa-118">Este parámetro no se utiliza y debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5f8aa-119">*pbFileHash* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8aa-120">Un puntero a un búfer para recibir el valor hash del archivo.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="5f8aa-121">El parámetro *pcbFileHash* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5f8aa-122">*pcbFileHash* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8aa-123">Puntero a una variable **DWORD** que, en la entrada, contiene el tamaño, en bytes, del búfer *pbFileHash* y, en la salida, recibe el tamaño, en bytes, del valor hash.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="5f8aa-124">Para obtener el tamaño requerido del valor hash, pase **null** para el parámetro *pbFileHash* .</span><span class="sxs-lookup"><span data-stu-id="5f8aa-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="5f8aa-125">Esta función colocará el tamaño necesario, en bytes, del valor hash en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="5f8aa-126">Si el parámetro *pbFileHash* no es **null** y el tamaño no es lo suficientemente grande como para recibir el valor hash, esta función colocará el tamaño necesario, en bytes, en esta ubicación y devolverá los **\_ \_ datos de error**.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="5f8aa-127">*pHashAlgid* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8aa-128">Un puntero a una variable de [**\_ identificador de alg**](alg-id.md) para recibir el identificador del algoritmo utilizado para crear el valor hash.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="5f8aa-129">Este parámetro puede ser **null** si no se necesita esta información.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8aa-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f8aa-130">Return value</span></span>

<span data-ttu-id="5f8aa-131">Devuelve un código de estado que indica si la función se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="5f8aa-132">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5f8aa-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5f8aa-133">Return code</span></span>                                                                                               | <span data-ttu-id="5f8aa-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f8aa-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f8aa-135"><dt>**ERROR \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5f8aa-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="5f8aa-136">El archivo está firmado y se ha comprobado la firma.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="5f8aa-137"><dt>**ERROR \_ más \_ datos**</dt></span><span class="sxs-lookup"><span data-stu-id="5f8aa-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="5f8aa-138">El parámetro *pbFileHash* no es **null** y el tamaño especificado por el parámetro *pcbFileHash* no es lo suficientemente grande como para recibir el hash.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="5f8aa-139"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f8aa-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="5f8aa-140">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="5f8aa-141"><dt>**CONFIANZA \_ E \_ \_ Resumen incorrecto**</dt></span><span class="sxs-lookup"><span data-stu-id="5f8aa-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="5f8aa-142">No se ha comprobado la firma del archivo.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="5f8aa-143"><dt>**CONFIAR \_ E \_ nofirma**</dt></span><span class="sxs-lookup"><span data-stu-id="5f8aa-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="5f8aa-144">El archivo no estaba firmado o tenía una firma no válida.</span><span class="sxs-lookup"><span data-stu-id="5f8aa-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="5f8aa-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f8aa-145">Requirements</span></span>



| <span data-ttu-id="5f8aa-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f8aa-146">Requirement</span></span> | <span data-ttu-id="5f8aa-147">Value</span><span class="sxs-lookup"><span data-stu-id="5f8aa-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8aa-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f8aa-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8aa-149">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5f8aa-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f8aa-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8aa-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f8aa-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f8aa-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f8aa-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f8aa-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f8aa-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
