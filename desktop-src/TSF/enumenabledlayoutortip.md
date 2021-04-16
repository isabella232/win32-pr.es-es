---
title: EnumEnabledLayoutOrTip función)
description: Enumera todas las distribuciones de teclado habilitadas o servicios de texto de la configuración de usuario especificada.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip función de servicios de texto
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685970"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="b70c7-104">EnumEnabledLayoutOrTip función)</span><span class="sxs-lookup"><span data-stu-id="b70c7-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="b70c7-105">Enumera todas las distribuciones de teclado habilitadas o servicios de texto de la configuración de usuario especificada.</span><span class="sxs-lookup"><span data-stu-id="b70c7-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70c7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b70c7-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="b70c7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b70c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70c7-108">*pszUserReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b70c7-109">La ruta de acceso del registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="b70c7-109">The registry path of the user.</span></span> <span data-ttu-id="b70c7-110">Si este parámetro es **null**, \_ \_ se utiliza HKEY current user.</span><span class="sxs-lookup"><span data-stu-id="b70c7-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="b70c7-111">*pszSystemReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b70c7-112">Ruta de acceso del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="b70c7-112">The registry path of the system.</span></span> <span data-ttu-id="b70c7-113">Si este parámetro es **null**, \_ \_ se usa HKEY local Machine \\ System.</span><span class="sxs-lookup"><span data-stu-id="b70c7-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="b70c7-114">*pszSoftwareReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b70c7-115">La ruta de acceso del registro del software.</span><span class="sxs-lookup"><span data-stu-id="b70c7-115">The registry path of the software.</span></span> <span data-ttu-id="b70c7-116">Si este parámetro es **null**, \_ \_ se utiliza el software del equipo local HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="b70c7-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="b70c7-117">*pLayoutOrTipProfile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b70c7-118">Puntero al búfer que recibe la matriz LAYOUTORTIPPROFILE.</span><span class="sxs-lookup"><span data-stu-id="b70c7-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="b70c7-119">*uBufLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70c7-120">Longitud del búfer al que apunta *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="b70c7-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70c7-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b70c7-121">Return value</span></span>

<span data-ttu-id="b70c7-122">Si *pLayoutOrTipProfile* es **null**, el número de elementos de teclado que están habilitados en la configuración de usuario; de lo contrario, el número de elementos de teclado que se copian en *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="b70c7-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="b70c7-123">En los lenguajes del editor de métodos de entrada (IME), se devuelven todos los IME, incluso cuando solo se habilita un IME.</span><span class="sxs-lookup"><span data-stu-id="b70c7-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="b70c7-124">Por ejemplo, si un usuario tiene el nuevo IME rápido en CHT habilitado, la función **EnumEnabledLayoutOrTip** devuelve los 5 IME CHT.</span><span class="sxs-lookup"><span data-stu-id="b70c7-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b70c7-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b70c7-125">Remarks</span></span>

<span data-ttu-id="b70c7-126">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="b70c7-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="b70c7-127">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="b70c7-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="b70c7-128">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b70c7-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="b70c7-129">La definición de LAYOUTORTIPPROFILE es:</span><span class="sxs-lookup"><span data-stu-id="b70c7-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="b70c7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b70c7-130">Requirements</span></span>



| <span data-ttu-id="b70c7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b70c7-131">Requirement</span></span> | <span data-ttu-id="b70c7-132">Value</span><span class="sxs-lookup"><span data-stu-id="b70c7-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b70c7-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b70c7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b70c7-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b70c7-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b70c7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b70c7-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b70c7-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b70c7-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b70c7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b70c7-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b70c7-138"><dt>Input.dll</dt></span></span> </dl> |



 

