---
title: CENUMNS. CPP
description: En el componente de proveedor de ejemplo, la enumeración de un objeto de espacio de nombres usa los métodos, desde cenumns. cpp, que se enumeran en la tabla siguiente.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656391"
---
# <a name="cenumnscpp"></a><span data-ttu-id="42159-103">CENUMNS. CPP</span><span class="sxs-lookup"><span data-stu-id="42159-103">CENUMNS.CPP</span></span>

<span data-ttu-id="42159-104">En el componente de proveedor de ejemplo, la enumeración de un objeto de espacio de nombres usa los métodos, desde cenumns. cpp, que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="42159-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="42159-105">Método</span><span class="sxs-lookup"><span data-stu-id="42159-105">Method</span></span>                                              | <span data-ttu-id="42159-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="42159-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42159-107">**CSampleDSNamespaceEnum:: Create**</span><span class="sxs-lookup"><span data-stu-id="42159-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="42159-108">Cree un objeto para permitir la enumeración de un objeto de espacio de nombres ADS.</span><span class="sxs-lookup"><span data-stu-id="42159-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="42159-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="42159-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="42159-110">Constructor estándar.</span><span class="sxs-lookup"><span data-stu-id="42159-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="42159-111">**CSampleDSNamespaceEnum:: ~ CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="42159-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="42159-112">Destructor estándar.</span><span class="sxs-lookup"><span data-stu-id="42159-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="42159-113">**CSampleDSNamespaceEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="42159-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="42159-114">Recupera el número especificado de elementos del objeto de espacio de nombres indicado.</span><span class="sxs-lookup"><span data-stu-id="42159-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="42159-115">**CSampleDSNamespaceEnum:: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="42159-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="42159-116">Administrar la recuperación de punteros de interfaz a los objetos.</span><span class="sxs-lookup"><span data-stu-id="42159-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="42159-117">**CSampleDSNamespaceEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="42159-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="42159-118">Recupera el conjunto de punteros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="42159-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="42159-119">**CSampleDSNamespaceEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="42159-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="42159-120">Captura el siguiente objeto.</span><span class="sxs-lookup"><span data-stu-id="42159-120">Fetch the next object.</span></span> <span data-ttu-id="42159-121">Si se encuentra, cree un objeto de Active Directory genérico y recupere su puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="42159-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 