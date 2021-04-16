---
description: Crea un enumerador para los formatos de transferencia que admite el dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'IWiaTransfer:: EnumWIA_FORMAT_INFO (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686830"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="11ab5-103">Método de información de \_ formato IWiaTransfer:: EnumWIA \_</span><span class="sxs-lookup"><span data-stu-id="11ab5-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="11ab5-104">Crea un enumerador para los formatos de transferencia que admite el dispositivo de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="11ab5-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ab5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11ab5-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="11ab5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11ab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ab5-107">*ppIEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11ab5-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11ab5-108">Tipo: **[ **\_ \_ información de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="11ab5-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="11ab5-109">Dirección del puntero a la interfaz de [**\_ \_ información de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) para el enumerador.</span><span class="sxs-lookup"><span data-stu-id="11ab5-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ab5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11ab5-110">Return value</span></span>

<span data-ttu-id="11ab5-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="11ab5-111">Type: **HRESULT**</span></span>

<span data-ttu-id="11ab5-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="11ab5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11ab5-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11ab5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ab5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11ab5-114">Remarks</span></span>

<span data-ttu-id="11ab5-115">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz recibido a través del parámetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="11ab5-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ab5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11ab5-116">Requirements</span></span>



| <span data-ttu-id="11ab5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="11ab5-117">Requirement</span></span> | <span data-ttu-id="11ab5-118">Value</span><span class="sxs-lookup"><span data-stu-id="11ab5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11ab5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11ab5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="11ab5-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11ab5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11ab5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11ab5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="11ab5-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11ab5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="11ab5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11ab5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11ab5-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="11ab5-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="11ab5-125">IDL</span><span class="sxs-lookup"><span data-stu-id="11ab5-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11ab5-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11ab5-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="11ab5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11ab5-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="11ab5-128"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11ab5-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
