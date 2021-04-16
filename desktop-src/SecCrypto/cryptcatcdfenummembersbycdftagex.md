---
description: Enumera los miembros de archivo individuales de la sección CatalogFiles de un archivo de definición de catálogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541003"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="8da1a-103">CryptCATCDFEnumMembersByCDFTagEx función)</span><span class="sxs-lookup"><span data-stu-id="8da1a-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="8da1a-104">\[La función **CryptCATCDFEnumMembersByCDFTagEx** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8da1a-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8da1a-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8da1a-106">La función **CryptCATCDFEnumMembersByCDFTagEx** enumera los miembros de archivo individuales en la sección **CatalogFiles** de un archivo de definición de catálogo (CDF).</span><span class="sxs-lookup"><span data-stu-id="8da1a-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="8da1a-107">[MakeCat](makecat.md)llama a **CryptCATCDFEnumMembersByCDFTagEx** .</span><span class="sxs-lookup"><span data-stu-id="8da1a-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="8da1a-108">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="8da1a-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="8da1a-109">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="8da1a-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8da1a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8da1a-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="8da1a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8da1a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da1a-112">*pCDF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da1a-113">Puntero a una estructura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="8da1a-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8da1a-114">*pwszPrevCDFTag* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8da1a-115">Puntero a una cadena terminada en **null** que identifica el miembro del archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="8da1a-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="8da1a-116">*pfnParseError* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da1a-117">Puntero a una función definida por el usuario para controlar los errores de análisis de archivos.</span><span class="sxs-lookup"><span data-stu-id="8da1a-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="8da1a-118">*ppMember* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da1a-119">Puntero a una estructura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contiene la información del miembro de archivo.</span><span class="sxs-lookup"><span data-stu-id="8da1a-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="8da1a-120">*fContinueOnError* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da1a-121">Valor que especifica si se debe mantener en memoria una referencia al último miembro enumerado.</span><span class="sxs-lookup"><span data-stu-id="8da1a-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="8da1a-122">*pvReserved* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da1a-123">Este parámetro está reservado; no lo utilice.</span><span class="sxs-lookup"><span data-stu-id="8da1a-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da1a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8da1a-124">Return value</span></span>

<span data-ttu-id="8da1a-125">Cuando se realiza correctamente, esta función devuelve un puntero a una cadena terminada en **null** que identifica un miembro de archivo en la sección **CATALOGFILES** de un CDF.</span><span class="sxs-lookup"><span data-stu-id="8da1a-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="8da1a-126">La función **CryptCATCDFEnumMembersByCDFTagEx** devuelve un puntero **null** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8da1a-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="8da1a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8da1a-127">Remarks</span></span>

<span data-ttu-id="8da1a-128">Normalmente, se llama a esta función en un bucle para enumerar todos los miembros del archivo de catálogo en un CDF.</span><span class="sxs-lookup"><span data-stu-id="8da1a-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="8da1a-129">Antes de entrar en el bucle, establezca *pwszPrevCDFTag* en **null**.</span><span class="sxs-lookup"><span data-stu-id="8da1a-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="8da1a-130">La función devuelve un puntero al primer miembro.</span><span class="sxs-lookup"><span data-stu-id="8da1a-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="8da1a-131">Establezca *pwszPrevCDFTag* en el valor devuelto de la función para las iteraciones posteriores del bucle.</span><span class="sxs-lookup"><span data-stu-id="8da1a-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="8da1a-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8da1a-132">Examples</span></span>

<span data-ttu-id="8da1a-133">En el ejemplo siguiente se muestra la secuencia correcta de asignaciones para el parámetro *pwszPrevCDFTag* ( `pwszMemberTag` ).</span><span class="sxs-lookup"><span data-stu-id="8da1a-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="8da1a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da1a-134">Requirements</span></span>



| <span data-ttu-id="8da1a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da1a-135">Requirement</span></span> | <span data-ttu-id="8da1a-136">Value</span><span class="sxs-lookup"><span data-stu-id="8da1a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8da1a-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8da1a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8da1a-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8da1a-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8da1a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8da1a-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8da1a-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8da1a-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8da1a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8da1a-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8da1a-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da1a-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="8da1a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da1a-144">MakeCat</span><span class="sxs-lookup"><span data-stu-id="8da1a-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="8da1a-145">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="8da1a-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="8da1a-146">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="8da1a-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="8da1a-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="8da1a-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="8da1a-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="8da1a-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
