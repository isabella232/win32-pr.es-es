---
description: Obtiene el IMFDXGIDeviceManager del receptor de representación de vídeo Microsoft Media Foundation.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'IMFDXGIDeviceManagerSource:: GetManager (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697025"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="4ebaf-103">IMFDXGIDeviceManagerSource:: GetManager (método)</span><span class="sxs-lookup"><span data-stu-id="4ebaf-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="4ebaf-104">Obtiene el [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) del receptor de representación de vídeo Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4ebaf-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebaf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ebaf-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="4ebaf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ebaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ebaf-107">*ppManager* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ebaf-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebaf-108">El objeto [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="4ebaf-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ebaf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ebaf-109">Return value</span></span>

<span data-ttu-id="4ebaf-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4ebaf-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ebaf-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ebaf-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ebaf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ebaf-112">Requirements</span></span>



| <span data-ttu-id="4ebaf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebaf-113">Requirement</span></span> | <span data-ttu-id="4ebaf-114">Value</span><span class="sxs-lookup"><span data-stu-id="4ebaf-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebaf-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ebaf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebaf-116">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4ebaf-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4ebaf-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ebaf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebaf-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4ebaf-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="4ebaf-119">IDL</span><span class="sxs-lookup"><span data-stu-id="4ebaf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ebaf-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ebaf-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ebaf-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ebaf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebaf-122">**IMFDXGIDeviceManagerSource**</span><span class="sxs-lookup"><span data-stu-id="4ebaf-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




