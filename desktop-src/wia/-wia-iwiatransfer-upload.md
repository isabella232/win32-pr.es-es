---
description: Inicia una carga de datos de un único elemento del llamador.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'IWiaTransfer:: upload (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275458"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="9e72d-103">IWiaTransfer:: upload (método)</span><span class="sxs-lookup"><span data-stu-id="9e72d-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="9e72d-104">Inicia una carga de datos de un único elemento del llamador.</span><span class="sxs-lookup"><span data-stu-id="9e72d-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e72d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e72d-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="9e72d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e72d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e72d-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e72d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e72d-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="9e72d-108">Type: **LONG**</span></span>

<span data-ttu-id="9e72d-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="9e72d-109">Currently unused.</span></span> <span data-ttu-id="9e72d-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="9e72d-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e72d-111">*pSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e72d-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e72d-112">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="9e72d-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="9e72d-113">Especifica un puntero a los datos de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="9e72d-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="9e72d-114">_pIWiaTransferCallback \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9e72d-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e72d-115">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="9e72d-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="9e72d-116">Especifica un puntero a la interfaz [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) del llamador.</span><span class="sxs-lookup"><span data-stu-id="9e72d-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e72d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e72d-117">Return value</span></span>

<span data-ttu-id="9e72d-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9e72d-118">Type: **HRESULT**</span></span>

<span data-ttu-id="9e72d-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9e72d-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e72d-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e72d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e72d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e72d-121">Requirements</span></span>



| <span data-ttu-id="9e72d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e72d-122">Requirement</span></span> | <span data-ttu-id="9e72d-123">Value</span><span class="sxs-lookup"><span data-stu-id="9e72d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e72d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e72d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e72d-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e72d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e72d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e72d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e72d-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e72d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e72d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e72d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e72d-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e72d-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="9e72d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="9e72d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e72d-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e72d-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="9e72d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e72d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e72d-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e72d-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
