---
description: La clase CHString expone los métodos siguientes.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Métodos CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082866"
---
# <a name="chstring-methods"></a><span data-ttu-id="1374b-103">Métodos CHString</span><span class="sxs-lookup"><span data-stu-id="1374b-103">CHString Methods</span></span>

<span data-ttu-id="1374b-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="1374b-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1374b-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="1374b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1374b-106">La clase [**CHString**](chstring.md) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="1374b-106">The [**CHString**](chstring.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1374b-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1374b-107">In this section</span></span>

-   [<span data-ttu-id="1374b-108">**Método AllocSysString**</span><span class="sxs-lookup"><span data-stu-id="1374b-108">**AllocSysString method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   <span data-ttu-id="1374b-109">[**Constructores CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="1374b-109">[**CHString constructors**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span></span>
-   [<span data-ttu-id="1374b-110">**COLLATE (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-110">**Collate method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [<span data-ttu-id="1374b-111">**Compare (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-111">**Compare method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [<span data-ttu-id="1374b-112">**Método CompareNoCase**</span><span class="sxs-lookup"><span data-stu-id="1374b-112">**CompareNoCase method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [<span data-ttu-id="1374b-113">**Empty (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-113">**Empty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   <span data-ttu-id="1374b-114">[**Métodos de búsqueda**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span><span class="sxs-lookup"><span data-stu-id="1374b-114">[**Find methods**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span></span>
-   [<span data-ttu-id="1374b-115">**Método FindOneOf**</span><span class="sxs-lookup"><span data-stu-id="1374b-115">**FindOneOf method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   <span data-ttu-id="1374b-116">[**Métodos de formato**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span><span class="sxs-lookup"><span data-stu-id="1374b-116">[**Format methods**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span></span>
-   <span data-ttu-id="1374b-117">[**Métodos FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span><span class="sxs-lookup"><span data-stu-id="1374b-117">[**FormatMessageW methods**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span></span>
-   [<span data-ttu-id="1374b-118">**Método FormatV**</span><span class="sxs-lookup"><span data-stu-id="1374b-118">**FormatV method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [<span data-ttu-id="1374b-119">**Método FreeExtra**</span><span class="sxs-lookup"><span data-stu-id="1374b-119">**FreeExtra method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [<span data-ttu-id="1374b-120">**Método GetAllocLength**</span><span class="sxs-lookup"><span data-stu-id="1374b-120">**GetAllocLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   <span data-ttu-id="1374b-121">[**GetAt (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span><span class="sxs-lookup"><span data-stu-id="1374b-121">[**GetAt method**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span></span>
-   [<span data-ttu-id="1374b-122">**GetBuffer (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-122">**GetBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [<span data-ttu-id="1374b-123">**Método GetBufferSetLength**</span><span class="sxs-lookup"><span data-stu-id="1374b-123">**GetBufferSetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [<span data-ttu-id="1374b-124">**Método GetData**</span><span class="sxs-lookup"><span data-stu-id="1374b-124">**GetData method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [<span data-ttu-id="1374b-125">**GetLength (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-125">**GetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [<span data-ttu-id="1374b-126">**IsEmpty (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-126">**IsEmpty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [<span data-ttu-id="1374b-127">**Left (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-127">**Left method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   <span data-ttu-id="1374b-128">[**Método LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span><span class="sxs-lookup"><span data-stu-id="1374b-128">[**LoadStringW method**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span></span>
-   [<span data-ttu-id="1374b-129">**Método LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="1374b-129">**LockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [<span data-ttu-id="1374b-130">**Método MakeLower**</span><span class="sxs-lookup"><span data-stu-id="1374b-130">**MakeLower method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [<span data-ttu-id="1374b-131">**Método MakeReverse**</span><span class="sxs-lookup"><span data-stu-id="1374b-131">**MakeReverse method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [<span data-ttu-id="1374b-132">**Método MakeUpper**</span><span class="sxs-lookup"><span data-stu-id="1374b-132">**MakeUpper method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   <span data-ttu-id="1374b-133">[**Métodos MID**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="1374b-133">[**Mid methods**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>
-   <span data-ttu-id="1374b-134">[**Operator ( \[ \] método)**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-134">[**operator\[\] method**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span></span>
-   [<span data-ttu-id="1374b-135">**CHString:: Operator +**</span><span class="sxs-lookup"><span data-stu-id="1374b-135">**CHString::operator+**</span></span>](chstring--operator-plus.md)
-   [<span data-ttu-id="1374b-136">**CHString:: Operator + =**</span><span class="sxs-lookup"><span data-stu-id="1374b-136">**CHString::operator+=**</span></span>](chstring--operator-plus-equal.md)
-   [<span data-ttu-id="1374b-137">**CHString:: Operator =**</span><span class="sxs-lookup"><span data-stu-id="1374b-137">**CHString::operator=**</span></span>](chstring--operator-equal.md)
-   <span data-ttu-id="1374b-138">[**Operator = = (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-138">[**operator==(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-139">[**Operator = = (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-139">[**operator==(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-140">[**Operator> (método constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-140">[**operator>(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-141">[**Operator> (método constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-141">[**operator>(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-142">[**Operator>= (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-142">[**operator>=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-143">[**Operator>= (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-143">[**operator>=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-144">[**Operator< (método constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-144">[**operator<(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-145">[**Operator< (método constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-145">[**operator<(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-146">[**Operator<= (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-146">[**operator<=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-147">[**Operator<= (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-147">[**operator<=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-148">[**Operator! = (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-148">[**operator!=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span></span>
-   <span data-ttu-id="1374b-149">[**Operator! = (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1374b-149">[**operator!=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span></span>
-   [<span data-ttu-id="1374b-150">**Operator LPCWSTR (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-150">**operator LPCWSTR method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [<span data-ttu-id="1374b-151">**Método ReleaseBuffer**</span><span class="sxs-lookup"><span data-stu-id="1374b-151">**ReleaseBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [<span data-ttu-id="1374b-152">**Método ReverseFind**</span><span class="sxs-lookup"><span data-stu-id="1374b-152">**ReverseFind method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [<span data-ttu-id="1374b-153">**Right (método)**</span><span class="sxs-lookup"><span data-stu-id="1374b-153">**Right method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [<span data-ttu-id="1374b-154">**Método SetAt**</span><span class="sxs-lookup"><span data-stu-id="1374b-154">**SetAt method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [<span data-ttu-id="1374b-155">**Método SpanExcluding**</span><span class="sxs-lookup"><span data-stu-id="1374b-155">**SpanExcluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [<span data-ttu-id="1374b-156">**Método SpanIncluding**</span><span class="sxs-lookup"><span data-stu-id="1374b-156">**SpanIncluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [<span data-ttu-id="1374b-157">**Método TrimLeft**</span><span class="sxs-lookup"><span data-stu-id="1374b-157">**TrimLeft method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [<span data-ttu-id="1374b-158">**Método TrimRight**</span><span class="sxs-lookup"><span data-stu-id="1374b-158">**TrimRight method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [<span data-ttu-id="1374b-159">**Método UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="1374b-159">**UnlockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
