---
description: Inicia una descarga de datos en el autor de la llamada.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: IWiaTransfer::D método scargar (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541966"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="d01b6-103">IWiaTransfer::D método scargar</span><span class="sxs-lookup"><span data-stu-id="d01b6-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="d01b6-104">Inicia una descarga de datos en el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d01b6-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d01b6-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="d01b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d01b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d01b6-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d01b6-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d01b6-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="d01b6-108">Type: **LONG**</span></span>

<span data-ttu-id="d01b6-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="d01b6-109">Currently unused.</span></span> <span data-ttu-id="d01b6-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="d01b6-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d01b6-111">*pIWiaTransferCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d01b6-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d01b6-112">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d01b6-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="d01b6-113">Especifica un puntero a la interfaz [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) del llamador.</span><span class="sxs-lookup"><span data-stu-id="d01b6-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d01b6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d01b6-114">Return value</span></span>

<span data-ttu-id="d01b6-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d01b6-115">Type: **HRESULT**</span></span>

<span data-ttu-id="d01b6-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d01b6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d01b6-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d01b6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d01b6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d01b6-118">Remarks</span></span>

<span data-ttu-id="d01b6-119">Si se descarga una carpeta, también se transfieren todos los elementos secundarios de dicha carpeta.</span><span class="sxs-lookup"><span data-stu-id="d01b6-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="d01b6-120">Cada elemento se transfiere en una secuencia independiente.</span><span class="sxs-lookup"><span data-stu-id="d01b6-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01b6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01b6-121">Requirements</span></span>



| <span data-ttu-id="d01b6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01b6-122">Requirement</span></span> | <span data-ttu-id="d01b6-123">Value</span><span class="sxs-lookup"><span data-stu-id="d01b6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d01b6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d01b6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d01b6-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d01b6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d01b6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d01b6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d01b6-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d01b6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d01b6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d01b6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d01b6-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d01b6-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="d01b6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d01b6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d01b6-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d01b6-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="d01b6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d01b6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d01b6-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d01b6-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




