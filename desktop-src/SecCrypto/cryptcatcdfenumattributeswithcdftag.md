---
description: Enumera los atributos de los archivos de miembro en la sección CatalogFiles de un archivo de definición de catálogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540998"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="edb9c-103">CryptCATCDFEnumAttributesWithCDFTag función)</span><span class="sxs-lookup"><span data-stu-id="edb9c-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="edb9c-104">\[La función **CryptCATCDFEnumAttributesWithCDFTag** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="edb9c-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="edb9c-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="edb9c-106">La función **CryptCATCDFEnumAttributesWithCDFTag** enumera los atributos de los archivos de miembro en la sección **CatalogFiles** de un archivo de definición de catálogo (CDF).</span><span class="sxs-lookup"><span data-stu-id="edb9c-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="edb9c-107">[MakeCat](makecat.md)llama a **CryptCATCDFEnumAttributesWithCDFTag** .</span><span class="sxs-lookup"><span data-stu-id="edb9c-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="edb9c-108">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="edb9c-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="edb9c-109">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="edb9c-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="edb9c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edb9c-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="edb9c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edb9c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb9c-112">*pCDF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb9c-113">Puntero a una estructura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="edb9c-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="edb9c-114">*pwszMemberTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb9c-115">Puntero a una cadena terminada en **null** que identifica el miembro del archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="edb9c-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="edb9c-116">*pMember* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb9c-117">Puntero a una estructura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contiene la información del miembro.</span><span class="sxs-lookup"><span data-stu-id="edb9c-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="edb9c-118">*pPrevAttr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb9c-119">Puntero a una estructura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) para un atributo de miembro de archivo en el CDF al que apunta *pCDF*.</span><span class="sxs-lookup"><span data-stu-id="edb9c-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="edb9c-120">*pfnParseError* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb9c-121">Puntero a una función definida por el usuario para controlar los errores de análisis de archivos.</span><span class="sxs-lookup"><span data-stu-id="edb9c-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb9c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb9c-122">Return value</span></span>

<span data-ttu-id="edb9c-123">Cuando se realiza correctamente, esta función devuelve un puntero a una estructura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) .</span><span class="sxs-lookup"><span data-stu-id="edb9c-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="edb9c-124">La función **CryptCATCDFEnumAttributesWithCDFTag** devuelve un puntero **null** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="edb9c-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb9c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edb9c-125">Remarks</span></span>

<span data-ttu-id="edb9c-126">Normalmente, se llama a esta función en un bucle para enumerar todos los atributos de los miembros del archivo de catálogo en un CDF.</span><span class="sxs-lookup"><span data-stu-id="edb9c-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="edb9c-127">Antes de entrar en el bucle, establezca *pPrevAttr* en **null**.</span><span class="sxs-lookup"><span data-stu-id="edb9c-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="edb9c-128">La función devuelve un puntero al primer atributo.</span><span class="sxs-lookup"><span data-stu-id="edb9c-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="edb9c-129">Establezca *pPrevAttr* en el valor devuelto de la función para las iteraciones posteriores del bucle.</span><span class="sxs-lookup"><span data-stu-id="edb9c-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="edb9c-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="edb9c-130">Examples</span></span>

<span data-ttu-id="edb9c-131">En el ejemplo siguiente se muestra la secuencia correcta de asignaciones para el parámetro *pPrevAttr* ( `pAttr` ).</span><span class="sxs-lookup"><span data-stu-id="edb9c-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="edb9c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edb9c-132">Requirements</span></span>



| <span data-ttu-id="edb9c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb9c-133">Requirement</span></span> | <span data-ttu-id="edb9c-134">Value</span><span class="sxs-lookup"><span data-stu-id="edb9c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb9c-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edb9c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="edb9c-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="edb9c-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edb9c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="edb9c-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="edb9c-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="edb9c-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edb9c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edb9c-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edb9c-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb9c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="edb9c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb9c-142">MakeCat</span><span class="sxs-lookup"><span data-stu-id="edb9c-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="edb9c-143">**CRYPTCATATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="edb9c-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="edb9c-144">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="edb9c-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="edb9c-145">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="edb9c-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="edb9c-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="edb9c-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="edb9c-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="edb9c-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
