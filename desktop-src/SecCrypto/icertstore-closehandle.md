---
description: Cierra un identificador HCERTSTORE adquirido a través de la propiedad StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'ICertStore:: CloseHandle (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671849"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="3595d-103">ICertStore:: CloseHandle (método)</span><span class="sxs-lookup"><span data-stu-id="3595d-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="3595d-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="3595d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="3595d-105">El método **CloseHandle** cierra un identificador HCERTSTORE adquirido a través de la propiedad [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="3595d-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3595d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3595d-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="3595d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3595d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3595d-108">*hCertStore* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3595d-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3595d-109">Identificador de HCERTSTORE que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="3595d-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3595d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3595d-110">Return value</span></span>

<span data-ttu-id="3595d-111">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3595d-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="3595d-112">Un valor de **S \_ OK** indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3595d-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="3595d-113">Cualquier otro valor indica que se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="3595d-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3595d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3595d-114">Remarks</span></span>

<span data-ttu-id="3595d-115">Este método no libera el identificador HCERTSTORE contenido dentro de un objeto [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="3595d-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="3595d-116">Solo se debe usar para liberar un identificador de HCERTSTORE adquirido a través de la propiedad [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="3595d-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3595d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3595d-117">Requirements</span></span>



| <span data-ttu-id="3595d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3595d-118">Requirement</span></span> | <span data-ttu-id="3595d-119">Value</span><span class="sxs-lookup"><span data-stu-id="3595d-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3595d-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3595d-120">Redistributable</span></span><br/> | <span data-ttu-id="3595d-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3595d-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3595d-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3595d-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="3595d-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3595d-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3595d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3595d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3595d-125">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="3595d-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




