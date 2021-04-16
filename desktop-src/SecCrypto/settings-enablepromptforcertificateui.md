---
description: Establece o recupera un valor booleano que especifica si se pueden usar los mensajes de la interfaz de usuario para el firmante o la identidad de un remitente.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Propiedad settings. EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690540"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="99a5a-103">Propiedad settings. EnablePromptForCertificateUI</span><span class="sxs-lookup"><span data-stu-id="99a5a-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="99a5a-104">\[La propiedad **EnablePromptForCertificateUI** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="99a5a-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="99a5a-105">La propiedad **EnablePromptForCertificateUI** establece o recupera un valor booleano que especifica si se pueden usar los mensajes de la interfaz de usuario para el firmante o la identidad de un remitente.</span><span class="sxs-lookup"><span data-stu-id="99a5a-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a5a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99a5a-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="99a5a-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="99a5a-107">Property value</span></span>

<span data-ttu-id="99a5a-108">Si **es true**, se puede usar la interfaz de usuario para solicitar un firmante o la identidad del remitente.</span><span class="sxs-lookup"><span data-stu-id="99a5a-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="99a5a-109">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="99a5a-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="99a5a-110">Al establecer esta propiedad, no se deshabilitan las advertencias generadas antes de que se realice un uso de clave privada desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="99a5a-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99a5a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99a5a-111">Requirements</span></span>



| <span data-ttu-id="99a5a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="99a5a-112">Requirement</span></span> | <span data-ttu-id="99a5a-113">Value</span><span class="sxs-lookup"><span data-stu-id="99a5a-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99a5a-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="99a5a-114">Redistributable</span></span><br/> | <span data-ttu-id="99a5a-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="99a5a-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="99a5a-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99a5a-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="99a5a-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99a5a-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99a5a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="99a5a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a5a-119">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="99a5a-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




