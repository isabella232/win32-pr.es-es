---
description: Establece o recupera el contenido de texto no cifrado de un mensaje que se va a aplicar sobre. Esta es la propiedad predeterminada.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Propiedad EnvelopedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649802"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="71a02-104">Propiedad EnvelopedData. Content</span><span class="sxs-lookup"><span data-stu-id="71a02-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="71a02-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="71a02-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="71a02-106">En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="71a02-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="71a02-107">La propiedad de **contenido** establece o recupera el contenido de texto sin formato de un mensaje que se va a aplicar sobre.</span><span class="sxs-lookup"><span data-stu-id="71a02-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="71a02-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="71a02-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a02-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71a02-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="71a02-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="71a02-110">Property value</span></span>

<span data-ttu-id="71a02-111">El contenido de texto sin formato de un mensaje que se va a acercar.</span><span class="sxs-lookup"><span data-stu-id="71a02-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="71a02-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71a02-112">Remarks</span></span>

<span data-ttu-id="71a02-113">La configuración de esta propiedad debe realizarse antes de llamar al método de [**cifrado**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="71a02-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="71a02-114">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier contenido cifrado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="71a02-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a02-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a02-115">Requirements</span></span>



| <span data-ttu-id="71a02-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a02-116">Requirement</span></span> | <span data-ttu-id="71a02-117">Value</span><span class="sxs-lookup"><span data-stu-id="71a02-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71a02-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="71a02-118">End of client support</span></span><br/> | <span data-ttu-id="71a02-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71a02-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="71a02-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="71a02-120">End of server support</span></span><br/> | <span data-ttu-id="71a02-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71a02-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="71a02-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="71a02-122">Redistributable</span></span><br/>       | <span data-ttu-id="71a02-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="71a02-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="71a02-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71a02-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="71a02-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a02-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a02-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="71a02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a02-127">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="71a02-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
