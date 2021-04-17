---
description: Devuelve un objeto RecordList que muestra los productos que utilizan un componente instalado especificado.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Propiedad Installer. ClientsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653752"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="34bea-103">Propiedad Installer. ClientsEx</span><span class="sxs-lookup"><span data-stu-id="34bea-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="34bea-104">Esta propiedad devuelve un objeto [**RecordList**](recordlist-object.md) que muestra los productos que utilizan un componente instalado especificado.</span><span class="sxs-lookup"><span data-stu-id="34bea-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="34bea-105">Esta propiedad llama a [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span><span class="sxs-lookup"><span data-stu-id="34bea-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="34bea-106">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="34bea-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="34bea-107">Esta propiedad está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="34bea-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="34bea-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="34bea-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34bea-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="34bea-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="34bea-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="34bea-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34bea-111">Requirements</span></span>



| <span data-ttu-id="34bea-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="34bea-112">Requirement</span></span> | <span data-ttu-id="34bea-113">Value</span><span class="sxs-lookup"><span data-stu-id="34bea-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34bea-114">Versión</span><span class="sxs-lookup"><span data-stu-id="34bea-114">Version</span></span><br/> | <span data-ttu-id="34bea-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="34bea-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="34bea-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34bea-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="34bea-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34bea-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="34bea-118">IID</span><span class="sxs-lookup"><span data-stu-id="34bea-118">IID</span></span><br/>     | <span data-ttu-id="34bea-119">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="34bea-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="34bea-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="34bea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34bea-121">**MsiEnumClientsEx**</span><span class="sxs-lookup"><span data-stu-id="34bea-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




