---
description: Devuelve un objeto RecordList que proporciona la ruta de acceso completa de un componente instalado especificado.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Propiedad Installer. ComponentPathEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653693"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="7d13d-103">Propiedad Installer. ComponentPathEx</span><span class="sxs-lookup"><span data-stu-id="7d13d-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="7d13d-104">Esta propiedad devuelve un objeto [**RecordList**](recordlist-object.md) que proporciona la ruta de acceso completa de un componente instalado especificado.</span><span class="sxs-lookup"><span data-stu-id="7d13d-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="7d13d-105">Esta propiedad llama a [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span><span class="sxs-lookup"><span data-stu-id="7d13d-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="7d13d-106">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="7d13d-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="7d13d-107">Esta propiedad está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="7d13d-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="7d13d-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d13d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d13d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d13d-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="7d13d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7d13d-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="7d13d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d13d-111">Requirements</span></span>



| <span data-ttu-id="7d13d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d13d-112">Requirement</span></span> | <span data-ttu-id="7d13d-113">Value</span><span class="sxs-lookup"><span data-stu-id="7d13d-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d13d-114">Versión</span><span class="sxs-lookup"><span data-stu-id="7d13d-114">Version</span></span><br/> | <span data-ttu-id="7d13d-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d13d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="7d13d-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d13d-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d13d-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d13d-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="7d13d-118">IID</span><span class="sxs-lookup"><span data-stu-id="7d13d-118">IID</span></span><br/>     | <span data-ttu-id="7d13d-119">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7d13d-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="7d13d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d13d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d13d-121">**MsiGetComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="7d13d-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




