---
description: 'La propiedad Time es la hora actual en horas, minutos y segundos como una cadena de texto literal en el formato HH: MM: SS con un reloj de 24 horas.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propiedad Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680560"
---
# <a name="time-property"></a><span data-ttu-id="54e98-103">Propiedad Time</span><span class="sxs-lookup"><span data-stu-id="54e98-103">Time property</span></span>

<span data-ttu-id="54e98-104">La propiedad **Time** es la hora actual en horas, minutos y segundos como una cadena de texto literal en el formato HH: mm: SS con un reloj de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="54e98-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="54e98-105">Por ejemplo, la hora 6:57 p.m.</span><span class="sxs-lookup"><span data-stu-id="54e98-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="54e98-106">se representa mediante "18:57:00".</span><span class="sxs-lookup"><span data-stu-id="54e98-106">is represented by "18:57:00".</span></span> <span data-ttu-id="54e98-107">El formato del valor depende de la configuración regional del usuario y es el formato obtenido mediante la función [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) con la opción Time \_ FORCE24HOURFORMAT \| Time \_ NOTIMEMARKER.</span><span class="sxs-lookup"><span data-stu-id="54e98-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="54e98-108">El valor de esta propiedad se establece en el Windows Installer y no en el autor del paquete.</span><span class="sxs-lookup"><span data-stu-id="54e98-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e98-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54e98-109">Remarks</span></span>

<span data-ttu-id="54e98-110">Dado que se trata de una cadena de texto, no se puede usar en expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="54e98-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e98-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54e98-111">Requirements</span></span>



| <span data-ttu-id="54e98-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e98-112">Requirement</span></span> | <span data-ttu-id="54e98-113">Value</span><span class="sxs-lookup"><span data-stu-id="54e98-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e98-114">Versión</span><span class="sxs-lookup"><span data-stu-id="54e98-114">Version</span></span><br/> | <span data-ttu-id="54e98-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54e98-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="54e98-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54e98-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="54e98-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="54e98-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="54e98-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="54e98-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54e98-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54e98-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e98-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54e98-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
