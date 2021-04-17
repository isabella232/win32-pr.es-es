---
description: La propiedad Date es el mes, el día y el año actuales como una cadena de texto literal en formato MM/DD/AAAA.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653795"
---
# <a name="date-property"></a><span data-ttu-id="e772a-103">Date, propiedad</span><span class="sxs-lookup"><span data-stu-id="e772a-103">Date property</span></span>

<span data-ttu-id="e772a-104">La propiedad **Date** es el mes, el día y el año actuales como una cadena de texto literal en formato mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="e772a-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="e772a-105">Por ejemplo, la fecha 22 de junio de 2005 puede representarse como "06/22/2005".</span><span class="sxs-lookup"><span data-stu-id="e772a-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="e772a-106">El formato del valor depende de la configuración regional del usuario y es el formato obtenido mediante [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) con la \_ opción Date fechacorta.</span><span class="sxs-lookup"><span data-stu-id="e772a-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="e772a-107">El valor de esta propiedad se establece en el Windows Installer y no en el autor del paquete.</span><span class="sxs-lookup"><span data-stu-id="e772a-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="e772a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e772a-108">Remarks</span></span>

<span data-ttu-id="e772a-109">Dado que se trata de una cadena de texto, no se puede usar en expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="e772a-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e772a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e772a-110">Requirements</span></span>



| <span data-ttu-id="e772a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e772a-111">Requirement</span></span> | <span data-ttu-id="e772a-112">Value</span><span class="sxs-lookup"><span data-stu-id="e772a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e772a-113">Versión</span><span class="sxs-lookup"><span data-stu-id="e772a-113">Version</span></span><br/> | <span data-ttu-id="e772a-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e772a-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e772a-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e772a-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e772a-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e772a-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e772a-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e772a-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e772a-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e772a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e772a-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e772a-119">Properties</span></span>](properties.md)
</dt> </dl>

 

