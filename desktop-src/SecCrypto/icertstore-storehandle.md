---
description: Establece o recupera el identificador HCERTSTORE de un almacén de certificados.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'ICertStore:: StoreHandle (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690479"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="faca9-103">ICertStore:: StoreHandle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="faca9-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="faca9-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="faca9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="faca9-105">La propiedad **StoreHandle** establece o recupera el identificador HCERTSTORE de un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="faca9-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="faca9-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="faca9-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="faca9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faca9-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="faca9-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="faca9-108">Property value</span></span>

<span data-ttu-id="faca9-109">Identificador de HCERTSTORE del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="faca9-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="faca9-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="faca9-110">Error codes</span></span>

<span data-ttu-id="faca9-111">Si los métodos de acceso de propiedad **colocan \_ StoreHandle** y **Get \_ StoreHandle** se ejecutan correctamente, devuelven los valores \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="faca9-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="faca9-112">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="faca9-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="faca9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faca9-113">Remarks</span></span>

<span data-ttu-id="faca9-114">Debe llamar al método [**CloseHandle**](icertstore-closehandle.md) o a la función [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) para liberar el contexto.</span><span class="sxs-lookup"><span data-stu-id="faca9-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="faca9-115">Si establece la propiedad **StoreHandle** , se restablece el estado del objeto de [**almacén**](store.md) completo.</span><span class="sxs-lookup"><span data-stu-id="faca9-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="faca9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faca9-116">Requirements</span></span>



| <span data-ttu-id="faca9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="faca9-117">Requirement</span></span> | <span data-ttu-id="faca9-118">Value</span><span class="sxs-lookup"><span data-stu-id="faca9-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faca9-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="faca9-119">Redistributable</span></span><br/> | <span data-ttu-id="faca9-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="faca9-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="faca9-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="faca9-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="faca9-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faca9-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faca9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="faca9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faca9-124">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="faca9-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




