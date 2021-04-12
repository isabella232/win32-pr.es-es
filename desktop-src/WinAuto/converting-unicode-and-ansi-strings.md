---
title: Convertir cadenas ANSI y Unicode
description: Microsoft Active Accessibility usa cadenas Unicode, tal y como se define en el tipo de datos BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359190"
---
# <a name="converting-unicode-and-ansi-strings"></a><span data-ttu-id="a50ac-103">Convertir cadenas ANSI y Unicode</span><span class="sxs-lookup"><span data-stu-id="a50ac-103">Converting Unicode and ANSI Strings</span></span>

<span data-ttu-id="a50ac-104">Microsoft Active Accessibility usa cadenas Unicode, tal y como se define en el tipo de datos **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a50ac-104">Microsoft Active Accessibility uses Unicode strings as defined by the **BSTR** data type.</span></span> <span data-ttu-id="a50ac-105">Si la aplicación no usa cadenas Unicode, o si desea convertir cadenas para determinadas llamadas API, use las funciones de Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para realizar la conversión necesaria.</span><span class="sxs-lookup"><span data-stu-id="a50ac-105">If your application does not use Unicode strings, or if you want to convert strings for certain API calls, use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 functions to perform the necessary conversion.</span></span>

<span data-ttu-id="a50ac-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para convertir una cadena Unicode en una cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="a50ac-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) to convert a Unicode string to an ANSI string.</span></span> <span data-ttu-id="a50ac-107">La función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) convierte una cadena ANSI en una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="a50ac-107">The [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function converts an ANSI string to a Unicode string.</span></span>

<span data-ttu-id="a50ac-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) y [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) para asignar y liberar tipos de datos **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a50ac-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) to allocate and free **BSTR** data types.</span></span>

<span data-ttu-id="a50ac-109">Para obtener más información sobre estas funciones de cadena, vea sus referencias en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="a50ac-109">For more information about these string functions, see their references in the Windows Software Development Kit (SDK).</span></span>

 

 