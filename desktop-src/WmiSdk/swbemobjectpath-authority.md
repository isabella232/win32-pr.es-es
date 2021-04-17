---
description: La propiedad Authority del objeto SWbemObjectPath contiene una cadena que define el componente de autoridad de la ruta de acceso del objeto.
ms.assetid: f00e5759-03b4-4333-b89e-5f54db73c3b7
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Authority (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Authority
- ISWbemObjectPath.Authority
- ISWbemObjectPath.get_Authority
- ISWbemObjectPath.put_Authority
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2b452f37f9f8d36b33596e032a82441a3507d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717031"
---
# <a name="swbemobjectpathauthority-property"></a><span data-ttu-id="ca6f6-103">Propiedad SWbemObjectPath. Authority</span><span class="sxs-lookup"><span data-stu-id="ca6f6-103">SWbemObjectPath.Authority property</span></span>

<span data-ttu-id="ca6f6-104">La propiedad **Authority** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene una cadena que define el componente de autoridad de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-104">The **Authority** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains a string that defines the Authority component of the object path.</span></span> <span data-ttu-id="ca6f6-105">Para obtener más información, vea el parámetro *strAuthority* del método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) y [establezca la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="ca6f6-105">For more information, see the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="ca6f6-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ca6f6-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ca6f6-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ca6f6-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6f6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca6f6-108">Syntax</span></span>


```VB
SWbemObjectPath.Authority As String
```



## <a name="property-value"></a><span data-ttu-id="ca6f6-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca6f6-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ca6f6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca6f6-110">Requirements</span></span>



| <span data-ttu-id="ca6f6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca6f6-111">Requirement</span></span> | <span data-ttu-id="ca6f6-112">Value</span><span class="sxs-lookup"><span data-stu-id="ca6f6-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6f6-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca6f6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ca6f6-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca6f6-114">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca6f6-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca6f6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ca6f6-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca6f6-116">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca6f6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca6f6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca6f6-118"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca6f6-118"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca6f6-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ca6f6-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca6f6-120"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca6f6-120"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca6f6-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca6f6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca6f6-122"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca6f6-122"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca6f6-123">CLSID</span><span class="sxs-lookup"><span data-stu-id="ca6f6-123">CLSID</span></span><br/>                    | <span data-ttu-id="ca6f6-124">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="ca6f6-124">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="ca6f6-125">IID</span><span class="sxs-lookup"><span data-stu-id="ca6f6-125">IID</span></span><br/>                      | <span data-ttu-id="ca6f6-126">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="ca6f6-126">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




