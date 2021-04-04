---
description: Crea un árbol jerárquico de objetos IWiaItem2 para un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2:: CreateDevice (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909870"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="4a877-103">IWiaDevMgr2:: CreateDevice (método)</span><span class="sxs-lookup"><span data-stu-id="4a877-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="4a877-104">Crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a877-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a877-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a877-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="4a877-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a877-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a877-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a877-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="4a877-108">Type: **LONG**</span></span>

<span data-ttu-id="4a877-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="4a877-109">Currently unused.</span></span> <span data-ttu-id="4a877-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="4a877-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a877-111">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a877-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a877-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a877-112">Type: **BSTR**</span></span>

<span data-ttu-id="4a877-113">Especifica el identificador único del dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a877-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="4a877-114">*ppWiaItem2Root* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4a877-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a877-115">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4a877-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="4a877-116">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz en el árbol jerárquico para el dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a877-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a877-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a877-117">Return value</span></span>

<span data-ttu-id="4a877-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a877-118">Type: **HRESULT**</span></span>

<span data-ttu-id="4a877-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4a877-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a877-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a877-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a877-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a877-121">Remarks</span></span>

<span data-ttu-id="4a877-122">Las aplicaciones usan el método **IWiaDevMgr2:: CreateDevice** para crear un objeto de dispositivo para los dispositivos WIA 2,0 especificados por el parámetro bstrDeviceID.</span><span class="sxs-lookup"><span data-stu-id="4a877-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="4a877-123">Cuando devuelve, el método **IWiaDevMgr2:: CreateDevice** almacena una dirección de un puntero en el parámetro *ppWiaItem2Root*, que señala al elemento raíz del árbol de objetos [**IWiaItem2**](-wia-iwiaitem2.md) creados por **IWiaDevMgr2:: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="4a877-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="4a877-124">Las aplicaciones pueden utilizar este árbol de objetos para controlar y recuperar datos del dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a877-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="4a877-125">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros que reciben a través del parámetro *ppWiaItem2Root* .</span><span class="sxs-lookup"><span data-stu-id="4a877-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a877-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a877-126">Requirements</span></span>



| <span data-ttu-id="4a877-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a877-127">Requirement</span></span> | <span data-ttu-id="4a877-128">Value</span><span class="sxs-lookup"><span data-stu-id="4a877-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a877-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a877-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a877-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a877-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a877-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a877-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a877-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a877-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a877-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a877-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a877-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a877-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a877-135">IDL</span><span class="sxs-lookup"><span data-stu-id="4a877-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a877-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a877-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
