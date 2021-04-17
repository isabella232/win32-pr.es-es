---
description: La propiedad ComponentClients de solo lectura devuelve un objeto StringList que enumera el conjunto de clientes de un componente especificado.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Propiedad Installer. ComponentClients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653695"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="18284-103">Propiedad Installer. ComponentClients</span><span class="sxs-lookup"><span data-stu-id="18284-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="18284-104">La propiedad **ComponentClients** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de clientes de un componente especificado.</span><span class="sxs-lookup"><span data-stu-id="18284-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="18284-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="18284-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18284-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18284-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="18284-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="18284-107">Property value</span></span>

<span data-ttu-id="18284-108">GUID de cadena que representa el código de componente del componente.</span><span class="sxs-lookup"><span data-stu-id="18284-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="18284-109">Los códigos de componente se especifican en la columna ComponentId de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="18284-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18284-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18284-110">Remarks</span></span>

<span data-ttu-id="18284-111">Para enumerar los clientes de componentes, una aplicación puede recorrer en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="18284-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="18284-112">Dado que los clientes no están ordenados, todos los componentes nuevos tienen un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="18284-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="18284-113">Esto significa que la función puede devolver los clientes en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="18284-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="18284-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18284-114">Requirements</span></span>



| <span data-ttu-id="18284-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="18284-115">Requirement</span></span> | <span data-ttu-id="18284-116">Value</span><span class="sxs-lookup"><span data-stu-id="18284-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18284-117">Versión</span><span class="sxs-lookup"><span data-stu-id="18284-117">Version</span></span><br/> | <span data-ttu-id="18284-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="18284-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="18284-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18284-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="18284-120">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="18284-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="18284-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18284-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="18284-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18284-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="18284-123">IID</span><span class="sxs-lookup"><span data-stu-id="18284-123">IID</span></span><br/>     | <span data-ttu-id="18284-124">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="18284-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="18284-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="18284-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18284-126">**MsiEnumClients**</span><span class="sxs-lookup"><span data-stu-id="18284-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




