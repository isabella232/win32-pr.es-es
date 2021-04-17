---
description: Devuelve un objeto RecordList que muestra los componentes instalados.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Propiedad Installer. ComponentsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653801"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="53a05-103">Propiedad Installer. ComponentsEx</span><span class="sxs-lookup"><span data-stu-id="53a05-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="53a05-104">Esta propiedad devuelve un objeto [**RecordList**](recordlist-object.md) que muestra los componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="53a05-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="53a05-105">Esta propiedad llama a [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span><span class="sxs-lookup"><span data-stu-id="53a05-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="53a05-106">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="53a05-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="53a05-107">Esta propiedad está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="53a05-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="53a05-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53a05-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a05-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53a05-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="53a05-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53a05-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="53a05-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a05-111">Requirements</span></span>



| <span data-ttu-id="53a05-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a05-112">Requirement</span></span> | <span data-ttu-id="53a05-113">Value</span><span class="sxs-lookup"><span data-stu-id="53a05-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a05-114">Versión</span><span class="sxs-lookup"><span data-stu-id="53a05-114">Version</span></span><br/> | <span data-ttu-id="53a05-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="53a05-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="53a05-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53a05-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="53a05-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a05-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="53a05-118">IID</span><span class="sxs-lookup"><span data-stu-id="53a05-118">IID</span></span><br/>     | <span data-ttu-id="53a05-119">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="53a05-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="53a05-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a05-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a05-121">**MsiEnumComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="53a05-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




