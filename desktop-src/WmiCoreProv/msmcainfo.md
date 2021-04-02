---
description: Una clase base abstracta de la que se derivan todas las clases de datos del proveedor de la arquitectura de comprobación de equipo (MCA), como MSMCAInfo \_ RawMCAData. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Clase MSMCAInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082108"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="72339-104">Clase MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="72339-104">MSMCAInfo class</span></span>

<span data-ttu-id="72339-105">La clase **MSMCAInfo** es una clase base abstracta de la que se derivan todas las clases de datos del proveedor de la arquitectura de comprobación de equipo (MCA), como [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md).</span><span class="sxs-lookup"><span data-stu-id="72339-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="72339-106">El proveedor de MCA también tiene clases de eventos, que se derivan de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="72339-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="72339-107">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="72339-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="72339-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="72339-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="72339-109">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="72339-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72339-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72339-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="72339-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="72339-111">Members</span></span>

<span data-ttu-id="72339-112">La clase **MSMCAInfo** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="72339-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="72339-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72339-113">Requirements</span></span>



| <span data-ttu-id="72339-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="72339-114">Requirement</span></span> | <span data-ttu-id="72339-115">Value</span><span class="sxs-lookup"><span data-stu-id="72339-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72339-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72339-116">Minimum supported client</span></span><br/> | <span data-ttu-id="72339-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="72339-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="72339-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72339-118">Minimum supported server</span></span><br/> | <span data-ttu-id="72339-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72339-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="72339-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72339-120">Namespace</span></span><br/>                | <span data-ttu-id="72339-121">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="72339-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="72339-122">MOF</span><span class="sxs-lookup"><span data-stu-id="72339-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72339-123"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72339-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="72339-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72339-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72339-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72339-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72339-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="72339-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72339-127">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="72339-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="72339-128">**\_Encabezado MSMCAEvent**</span><span class="sxs-lookup"><span data-stu-id="72339-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="72339-129">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="72339-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




