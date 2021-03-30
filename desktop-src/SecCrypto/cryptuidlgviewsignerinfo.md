---
description: Muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Función CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907821"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="b0c78-103">Función CryptUIDlgViewSignerInfo</span><span class="sxs-lookup"><span data-stu-id="b0c78-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="b0c78-104">\[La función **CryptUIDlgViewSignerInfo** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b0c78-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b0c78-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b0c78-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b0c78-106">\]</span><span class="sxs-lookup"><span data-stu-id="b0c78-106">\]</span></span>

<span data-ttu-id="b0c78-107">La función **CryptUIDlgViewSignerInfo** muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="b0c78-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="b0c78-108">Esta función no se declara en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="b0c78-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="b0c78-109">Para usar esta estructura, declárela en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="b0c78-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0c78-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0c78-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="b0c78-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0c78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c78-112">*pcvsi* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0c78-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0c78-113">Puntero a una estructura de estructura [**CRYPTUI \_ VIEWSIGNERINFO \_**](cryptui-viewsignerinfo-struct.md) que contiene la información del firmante que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="b0c78-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0c78-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0c78-114">Return value</span></span>

<span data-ttu-id="b0c78-115">Esta función devuelve un valor distinto de cero si se realiza correctamente y cero en caso de error.</span><span class="sxs-lookup"><span data-stu-id="b0c78-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="b0c78-116">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="b0c78-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="b0c78-117">Los códigos de error posibles devueltos por [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b0c78-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b0c78-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b0c78-118">Return code</span></span>                                                                                   | <span data-ttu-id="b0c78-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0c78-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b0c78-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b0c78-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b0c78-121">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b0c78-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b0c78-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0c78-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b0c78-123">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="b0c78-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="b0c78-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0c78-124">Requirements</span></span>



| <span data-ttu-id="b0c78-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0c78-125">Requirement</span></span> | <span data-ttu-id="b0c78-126">Value</span><span class="sxs-lookup"><span data-stu-id="b0c78-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c78-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0c78-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c78-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b0c78-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b0c78-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0c78-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c78-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0c78-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0c78-131">Finalización del soporte técnico</span><span class="sxs-lookup"><span data-stu-id="b0c78-131">End of support</span></span><br/> | <span data-ttu-id="b0c78-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0c78-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b0c78-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0c78-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0c78-134"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0c78-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="b0c78-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0c78-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0c78-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0c78-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="b0c78-137">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b0c78-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b0c78-138">**CryptUIDlgViewSignerInfoW** (Unicode) y **CryptUIDlgViewSignerInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b0c78-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0c78-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0c78-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c78-140">**CRYPTUI \_ VIEWSIGNERINFO \_ struct**</span><span class="sxs-lookup"><span data-stu-id="b0c78-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
