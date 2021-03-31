---
title: CENUMSCH. CPP
description: En el componente de proveedor de ejemplo, la enumeración de un objeto de esquema usa los métodos, desde cenumsch. cpp, que se enumeran en la tabla siguiente.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903074"
---
# <a name="cenumschcpp"></a><span data-ttu-id="3ee1c-103">CENUMSCH. CPP</span><span class="sxs-lookup"><span data-stu-id="3ee1c-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="3ee1c-104">En el componente de proveedor de ejemplo, la enumeración de un objeto de esquema usa los métodos, desde cenumsch. cpp, que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="3ee1c-105">Método</span><span class="sxs-lookup"><span data-stu-id="3ee1c-105">Method</span></span>                                        | <span data-ttu-id="3ee1c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ee1c-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee1c-107">**CSampleDSSchemaEnum:: Create**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="3ee1c-108">Cree un objeto para permitir la enumeración de un objeto de clase de esquema ADSI.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="3ee1c-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="3ee1c-110">Constructor estándar.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="3ee1c-111">**CSampleDSSchemaEnum:: ~ CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="3ee1c-112">Destructor estándar.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="3ee1c-113">**CSampleDSSchemaEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="3ee1c-114">Recupera el número especificado de elementos del objeto de esquema indicado.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="3ee1c-115">**CSampleDSSchemaEnum:: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="3ee1c-116">Administrar la recuperación de los punteros de interfaz a los objetos del tipo de objeto indicado.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="3ee1c-117">**CSampleDSSchemaEnum:: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="3ee1c-118">Administrar la recuperación de los punteros de interfaz a los objetos del tipo de objeto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="3ee1c-119">**CSampleDSSchemaEnum::EnumClasses**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="3ee1c-120">Administrar la recuperación de punteros de interfaz únicamente a los objetos de clase de esquema incluidos en este objeto.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="3ee1c-121">**CSampleDSSchemaEnum:: Getclassobject (**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="3ee1c-122">Recupere la siguiente definición de clase de esquema; Si se encuentra, cree un objeto de clase de esquema y devuelva el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="3ee1c-123">**CSampleDSSchemaEnum:: EnumProperties (**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="3ee1c-124">Administrar la recuperación de los punteros de interfaz a los objetos de propiedad solo contenidos en este objeto.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="3ee1c-125">**CSampleDSSchemaEnum::GetPropertyObject**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="3ee1c-126">Recupera la definición de la propiedad siguiente; Si se encuentra, cree un objeto de clase de esquema y devuelva el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="3ee1c-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="3ee1c-128">Administrar la recuperación de punteros de interfaz a los objetos de sintaxis que solo contiene este objeto.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="3ee1c-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span><span class="sxs-lookup"><span data-stu-id="3ee1c-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="3ee1c-130">Recuperar la siguiente definición de sintaxis; Si se encuentra, cree un objeto de clase de esquema y devuelva el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3ee1c-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




