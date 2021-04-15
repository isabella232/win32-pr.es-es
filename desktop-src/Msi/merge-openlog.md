---
description: El método OpenLog del objeto Merge abre un archivo de registro que recibe los mensajes de progreso y de error. Si el archivo de registro ya existe, el instalador anexa los nuevos mensajes. Si el archivo de registro no existe, el instalador crea un archivo de registro.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Método Merge. OpenLog (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654023"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="dbec1-105">Merge. OpenLog (método)</span><span class="sxs-lookup"><span data-stu-id="dbec1-105">Merge.OpenLog method</span></span>

<span data-ttu-id="dbec1-106">El método **openlog** del objeto [**Merge**](merge-object.md) abre un archivo de registro que recibe los mensajes de progreso y de error.</span><span class="sxs-lookup"><span data-stu-id="dbec1-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="dbec1-107">Si el archivo de registro ya existe, el instalador anexa los nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="dbec1-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="dbec1-108">Si el archivo de registro no existe, el instalador crea un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="dbec1-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbec1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbec1-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="dbec1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbec1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbec1-111">*Nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="dbec1-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="dbec1-112">Nombre de archivo completo que apunta a un archivo para abrirlo o crearlo.</span><span class="sxs-lookup"><span data-stu-id="dbec1-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbec1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbec1-113">Return value</span></span>

<span data-ttu-id="dbec1-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dbec1-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbec1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbec1-115">Remarks</span></span>

<span data-ttu-id="dbec1-116">Los clientes pueden enviar sus propios mensajes a este archivo de registro a través del método [**log**](merge-log.md) .</span><span class="sxs-lookup"><span data-stu-id="dbec1-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="dbec1-117">C++</span><span class="sxs-lookup"><span data-stu-id="dbec1-117">C++</span></span>

<span data-ttu-id="dbec1-118">Consulte función [**openlog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .</span><span class="sxs-lookup"><span data-stu-id="dbec1-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbec1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbec1-119">Requirements</span></span>



| <span data-ttu-id="dbec1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbec1-120">Requirement</span></span> | <span data-ttu-id="dbec1-121">Value</span><span class="sxs-lookup"><span data-stu-id="dbec1-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbec1-122">Versión</span><span class="sxs-lookup"><span data-stu-id="dbec1-122">Version</span></span><br/> | <span data-ttu-id="dbec1-123">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dbec1-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="dbec1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbec1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dbec1-125"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbec1-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbec1-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbec1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbec1-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbec1-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
