---
description: El objeto ConfigureModule es una interfaz implementada por el cliente.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objeto ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653923"
---
# <a name="configuremodule-object"></a><span data-ttu-id="dff8f-103">Objeto ConfigureModule</span><span class="sxs-lookup"><span data-stu-id="dff8f-103">ConfigureModule object</span></span>

<span data-ttu-id="dff8f-104">El **objeto ConfigureModule** es una interfaz implementada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="dff8f-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="dff8f-105">Mergemod.dllllama a los métodos de la interfaz **IMsmConfigureModule** para solicitar que la herramienta cliente proporcione información de configuración.</span><span class="sxs-lookup"><span data-stu-id="dff8f-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="dff8f-106">El módulo se configura en función de las respuestas del cliente a las llamadas en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="dff8f-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="dff8f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dff8f-107">Members</span></span>

<span data-ttu-id="dff8f-108">El objeto **ConfigureModule** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dff8f-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="dff8f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dff8f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dff8f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dff8f-110">Methods</span></span>

<span data-ttu-id="dff8f-111">El objeto **ConfigureModule** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dff8f-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="dff8f-112">Método</span><span class="sxs-lookup"><span data-stu-id="dff8f-112">Method</span></span>                                                           | <span data-ttu-id="dff8f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dff8f-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="dff8f-114">**ProvideIntegerData**</span><span class="sxs-lookup"><span data-stu-id="dff8f-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="dff8f-115">Llamado por Mergemod.dll para obtener enteros utilizados para configurar el módulo.</span><span class="sxs-lookup"><span data-stu-id="dff8f-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="dff8f-116">**ProvideTextData**</span><span class="sxs-lookup"><span data-stu-id="dff8f-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="dff8f-117">Llamado por Mergemod.dll para obtener el texto que se usa para configurar el módulo.</span><span class="sxs-lookup"><span data-stu-id="dff8f-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="dff8f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dff8f-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="dff8f-119">C++</span><span class="sxs-lookup"><span data-stu-id="dff8f-119">C++</span></span>

<span data-ttu-id="dff8f-120">interfaz **IMsmConfigureModule: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="dff8f-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="dff8f-121">IDENTIFICADOR de interfaz</span><span class="sxs-lookup"><span data-stu-id="dff8f-121">Interface ID</span></span>



| <span data-ttu-id="dff8f-122">Constante</span><span class="sxs-lookup"><span data-stu-id="dff8f-122">Constant</span></span>                     | <span data-ttu-id="dff8f-123">Value</span><span class="sxs-lookup"><span data-stu-id="dff8f-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="dff8f-124">**\_IMSMCONFIGUREMODULE IID**</span><span class="sxs-lookup"><span data-stu-id="dff8f-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="dff8f-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="dff8f-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="dff8f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dff8f-126">Requirements</span></span>



| <span data-ttu-id="dff8f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dff8f-127">Requirement</span></span> | <span data-ttu-id="dff8f-128">Value</span><span class="sxs-lookup"><span data-stu-id="dff8f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dff8f-129">Versión</span><span class="sxs-lookup"><span data-stu-id="dff8f-129">Version</span></span><br/> | <span data-ttu-id="dff8f-130">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dff8f-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="dff8f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dff8f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="dff8f-132"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff8f-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="dff8f-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dff8f-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="dff8f-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dff8f-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




