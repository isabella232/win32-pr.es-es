---
description: En Windows Installer versiones 1,0 y 1,1, la propiedad path siempre es la cadena vacía. Las versiones futuras pueden utilizar este valor para devolver la ruta de acceso al archivo o directorio que no se pudo crear.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Propiedad error. Path (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690192"
---
# <a name="errorpath-property"></a><span data-ttu-id="3a2e1-104">Error. Path (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3a2e1-104">Error.Path property</span></span>

<span data-ttu-id="3a2e1-105">En Windows Installer versiones 1,0 y 1,1, la propiedad path siempre es la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="3a2e1-106">Las versiones futuras pueden utilizar este valor para devolver la ruta de acceso al archivo o directorio que no se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="3a2e1-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a2e1-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="3a2e1-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3a2e1-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2e1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a2e1-110">Remarks</span></span>

<span data-ttu-id="3a2e1-111">Este valor solo es válido para los errores de tipo msmErrorFileCreate o msmErrorDirCreate.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="3a2e1-112">Puede determinar el tipo de error mediante una llamada a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2e1-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="3a2e1-113">C++</span><span class="sxs-lookup"><span data-stu-id="3a2e1-113">C++</span></span>

<span data-ttu-id="3a2e1-114">Vea [**Get \_ path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2e1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2e1-115">Requirements</span></span>



| <span data-ttu-id="3a2e1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2e1-116">Requirement</span></span> | <span data-ttu-id="3a2e1-117">Value</span><span class="sxs-lookup"><span data-stu-id="3a2e1-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2e1-118">Versión</span><span class="sxs-lookup"><span data-stu-id="3a2e1-118">Version</span></span><br/> | <span data-ttu-id="3a2e1-119">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3a2e1-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3a2e1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a2e1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3a2e1-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e1-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a2e1-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a2e1-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a2e1-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e1-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

