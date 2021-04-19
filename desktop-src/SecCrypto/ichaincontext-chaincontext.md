---
description: Establece o recupera el \_ \_ contexto de la cadena de PCCERT de un certificado.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'IChainContext:: ChainContext (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690008"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="c084f-103">IChainContext:: ChainContext (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c084f-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="c084f-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="c084f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="c084f-105">La propiedad **ChainContext** establece o recupera el \_ \_ contexto de cadena PCCERT de un certificado.</span><span class="sxs-lookup"><span data-stu-id="c084f-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="c084f-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c084f-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c084f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c084f-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="c084f-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c084f-108">Property value</span></span>

<span data-ttu-id="c084f-109">El \_ \_ contexto de la cadena de PCCERT del certificado.</span><span class="sxs-lookup"><span data-stu-id="c084f-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c084f-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c084f-110">Error codes</span></span>

<span data-ttu-id="c084f-111">Si los métodos de acceso de propiedad **colocan \_ ChainContext** y **Get \_ ChainContext** se ejecutan correctamente, devuelven los valores \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="c084f-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="c084f-112">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="c084f-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c084f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c084f-113">Remarks</span></span>

<span data-ttu-id="c084f-114">Debe llamar al método [**FreeContext**](ichaincontext-freecontext.md) o a la función [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) para liberar el contexto.</span><span class="sxs-lookup"><span data-stu-id="c084f-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="c084f-115">Si establece la propiedad **ChainContext** , se restablece el estado del objeto de [**cadena**](chain.md) completo.</span><span class="sxs-lookup"><span data-stu-id="c084f-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="c084f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c084f-116">Requirements</span></span>



| <span data-ttu-id="c084f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c084f-117">Requirement</span></span> | <span data-ttu-id="c084f-118">Value</span><span class="sxs-lookup"><span data-stu-id="c084f-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c084f-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c084f-119">Redistributable</span></span><br/> | <span data-ttu-id="c084f-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="c084f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c084f-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c084f-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="c084f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c084f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c084f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c084f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c084f-124">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="c084f-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




