---
description: El método CerrarBaseDeDatos del objeto Merge cierra la base de datos de Windows Installer abierta actualmente.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge. CerrarBaseDeDatos (método) (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678875"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="6b330-103">Merge. CerrarBaseDeDatos (método)</span><span class="sxs-lookup"><span data-stu-id="6b330-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="6b330-104">El método **CerrarBaseDeDatos** del objeto [**Merge**](merge-object.md) cierra la base de datos de Windows Installer abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="6b330-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b330-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b330-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="6b330-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b330-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b330-107">*bCommit*</span><span class="sxs-lookup"><span data-stu-id="6b330-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="6b330-108">**True** si se deben guardar los cambios; en caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="6b330-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b330-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b330-109">Return value</span></span>

<span data-ttu-id="6b330-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6b330-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b330-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b330-111">Remarks</span></span>

<span data-ttu-id="6b330-112">Al cerrar una base de datos se borra toda la información de dependencias, pero no se afecta a los errores que no se hayan recuperado.</span><span class="sxs-lookup"><span data-stu-id="6b330-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="6b330-113">C++</span><span class="sxs-lookup"><span data-stu-id="6b330-113">C++</span></span>

<span data-ttu-id="6b330-114">Vea [**CerrarBaseDeDatos**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) (función).</span><span class="sxs-lookup"><span data-stu-id="6b330-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b330-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b330-115">Requirements</span></span>



| <span data-ttu-id="6b330-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b330-116">Requirement</span></span> | <span data-ttu-id="6b330-117">Value</span><span class="sxs-lookup"><span data-stu-id="6b330-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b330-118">Versión</span><span class="sxs-lookup"><span data-stu-id="6b330-118">Version</span></span><br/> | <span data-ttu-id="6b330-119">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6b330-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6b330-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b330-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6b330-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b330-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b330-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b330-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b330-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b330-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
