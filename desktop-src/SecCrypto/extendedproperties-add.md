---
description: Agrega una propiedad extendida a la colección.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: ExtendedProperties. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649953"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="f03b2-103">ExtendedProperties. Add (método)</span><span class="sxs-lookup"><span data-stu-id="f03b2-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="f03b2-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f03b2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f03b2-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="f03b2-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="f03b2-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="f03b2-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f03b2-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="f03b2-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f03b2-108">El método **Add** agrega una propiedad extendida a la colección.</span><span class="sxs-lookup"><span data-stu-id="f03b2-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03b2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f03b2-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="f03b2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f03b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03b2-111">*valProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f03b2-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03b2-112">Objeto [**ExtendedProperty**](extendedproperty.md) que representa la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="f03b2-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03b2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f03b2-113">Return value</span></span>

<span data-ttu-id="f03b2-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f03b2-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f03b2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f03b2-115">Requirements</span></span>



| <span data-ttu-id="f03b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f03b2-116">Requirement</span></span> | <span data-ttu-id="f03b2-117">Value</span><span class="sxs-lookup"><span data-stu-id="f03b2-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f03b2-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f03b2-118">End of client support</span></span><br/> | <span data-ttu-id="f03b2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f03b2-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f03b2-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f03b2-120">End of server support</span></span><br/> | <span data-ttu-id="f03b2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f03b2-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f03b2-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f03b2-122">Redistributable</span></span><br/>       | <span data-ttu-id="f03b2-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f03b2-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f03b2-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f03b2-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f03b2-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f03b2-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
