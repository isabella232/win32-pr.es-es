---
title: Interfaz IWMPLibraryServices (VB y C) (WMP. h)
description: Proporciona métodos para enumerar las bibliotecas.
ms.assetid: f2a72731-6e61-4f78-b0ca-ae907004eb7d
keywords:
- IWMPLibraryServices (VB y C) interfaz de Windows Media Player
- IWMPLibraryServices (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPLibraryServices (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3493d5c94dcbd9db1e4f281a8fddfadbd2e336f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690088"
---
# <a name="iwmplibraryservices-vb-and-c-interface"></a><span data-ttu-id="84fe0-105">Interfaz IWMPLibraryServices (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="84fe0-105">IWMPLibraryServices (VB and C#) interface</span></span>

<span data-ttu-id="84fe0-106">Proporciona métodos para enumerar las bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="84fe0-106">Provides methods to enumerate libraries.</span></span>

## <a name="members"></a><span data-ttu-id="84fe0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="84fe0-107">Members</span></span>

<span data-ttu-id="84fe0-108">La interfaz **IWMPLibraryServices (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="84fe0-108">The **IWMPLibraryServices (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="84fe0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="84fe0-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84fe0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="84fe0-110">Methods</span></span>

<span data-ttu-id="84fe0-111">La interfaz **IWMPLibraryServices (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="84fe0-111">The **IWMPLibraryServices (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="84fe0-112">Método</span><span class="sxs-lookup"><span data-stu-id="84fe0-112">Method</span></span>                                                                                               | <span data-ttu-id="84fe0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="84fe0-113">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84fe0-114">**getCountByType**</span><span class="sxs-lookup"><span data-stu-id="84fe0-114">**getCountByType**</span></span>](wmplibiwmplibraryservices-iwmplibraryservices-getcountbytype--vb-and-c.md)     | <span data-ttu-id="84fe0-115">Devuelve el número de bibliotecas disponibles de un tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="84fe0-115">Returns the count of available libraries of a specified type.</span></span><br/>                                           |
| [<span data-ttu-id="84fe0-116">**getLibraryByType**</span><span class="sxs-lookup"><span data-stu-id="84fe0-116">**getLibraryByType**</span></span>](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md) | <span data-ttu-id="84fe0-117">Devuelve una interfaz **IWMPLibrary** que representa la biblioteca que tiene el tipo y el índice especificados.</span><span class="sxs-lookup"><span data-stu-id="84fe0-117">Returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span><br/> |



 

<span data-ttu-id="84fe0-118">Obtenga una interfaz **IWMPLibraryServices** mediante la conversión del objeto devuelto desde el método **AxWindowsMediaPlayer. GetOcx** .</span><span class="sxs-lookup"><span data-stu-id="84fe0-118">Get an **IWMPLibraryServices** interface by casting the object returned from the **AxWindowsMediaPlayer.GetOcx** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fe0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84fe0-119">Requirements</span></span>



| <span data-ttu-id="84fe0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84fe0-120">Requirement</span></span> | <span data-ttu-id="84fe0-121">Value</span><span class="sxs-lookup"><span data-stu-id="84fe0-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84fe0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84fe0-122">Header</span></span><br/> | <dl> <span data-ttu-id="84fe0-123"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="84fe0-123"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84fe0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="84fe0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fe0-125">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="84fe0-125">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="84fe0-126">**Interfaz IWMPLibrary (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="84fe0-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





