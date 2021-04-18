---
description: Determina si una cadena Unicode coincide con el patrón especificado.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666175"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="9db6d-103">RtlIsNameInExpression función)</span><span class="sxs-lookup"><span data-stu-id="9db6d-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="9db6d-104">Determina si una cadena Unicode coincide con el patrón especificado.</span><span class="sxs-lookup"><span data-stu-id="9db6d-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db6d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9db6d-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="9db6d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9db6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db6d-107">*Expresión* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9db6d-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db6d-108">Puntero a la cadena de modelo.</span><span class="sxs-lookup"><span data-stu-id="9db6d-108">A pointer to the pattern string.</span></span> <span data-ttu-id="9db6d-109">Esta cadena puede contener caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="9db6d-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="9db6d-110">Si el parámetro *ignoreCase* es true, la cadena solo debe contener caracteres en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="9db6d-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="9db6d-111">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9db6d-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db6d-112">Puntero a la cadena que se va a comparar con el modelo.</span><span class="sxs-lookup"><span data-stu-id="9db6d-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="9db6d-113">Esta cadena no puede contener caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="9db6d-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="9db6d-114">*IgnoreCase* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9db6d-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db6d-115">**True** para la coincidencia sin distinción entre mayúsculas y minúsculas, o **false** para la coincidencia con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9db6d-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="9db6d-116">*UpcaseTable* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9db6d-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9db6d-117">Un puntero opcional a una tabla de caracteres en mayúsculas que se va a utilizar para la coincidencia sin distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9db6d-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="9db6d-118">Si este parámetro es NULL, se utiliza la tabla de caracteres en mayúsculas predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="9db6d-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db6d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9db6d-119">Return value</span></span>

<span data-ttu-id="9db6d-120">Devuelve **true** si la cadena coincide con el patrón.</span><span class="sxs-lookup"><span data-stu-id="9db6d-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="9db6d-121">Si la cadena no coincide con el patrón, esta función devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="9db6d-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db6d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9db6d-122">Remarks</span></span>

<span data-ttu-id="9db6d-123">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="9db6d-123">This function has no associated header file.</span></span> <span data-ttu-id="9db6d-124">La biblioteca de importación asociada, ntdll. lib, está disponible en el kit de controladores de Windows (WDK) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9db6d-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="9db6d-125">También puede llamar a esta función mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="9db6d-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db6d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9db6d-126">Requirements</span></span>



| <span data-ttu-id="9db6d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db6d-127">Requirement</span></span> | <span data-ttu-id="9db6d-128">Value</span><span class="sxs-lookup"><span data-stu-id="9db6d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9db6d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9db6d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9db6d-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9db6d-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9db6d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9db6d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9db6d-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9db6d-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9db6d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9db6d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db6d-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db6d-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
