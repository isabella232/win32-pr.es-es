---
description: Convierte la hora local del equipo en hora universal coordinada (hora del meridiano de Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities. LocalTimeToUTCTime (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689908"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="a8f3e-103">Utilities. LocalTimeToUTCTime (método)</span><span class="sxs-lookup"><span data-stu-id="a8f3e-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="a8f3e-104">\[El método **LocalTimeToUTCTime** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="a8f3e-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="a8f3e-105">El método **LocalTimeToUTCTime** convierte la hora local del equipo a la hora universal coordinada (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="a8f3e-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f3e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8f3e-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="a8f3e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8f3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f3e-108">*Localtime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8f3e-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f3e-109">La hora local que se va a convertir en hora universal coordinada.</span><span class="sxs-lookup"><span data-stu-id="a8f3e-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f3e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8f3e-110">Return value</span></span>

<span data-ttu-id="a8f3e-111">Hora universal coordinada que corresponde a la hora local especificada.</span><span class="sxs-lookup"><span data-stu-id="a8f3e-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f3e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8f3e-112">Remarks</span></span>

<span data-ttu-id="a8f3e-113">Aunque el sistema utiliza la hora universal coordinada internamente, las aplicaciones suelen mostrar la hora local, que es la fecha y la hora del día de la zona horaria local del equipo.</span><span class="sxs-lookup"><span data-stu-id="a8f3e-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f3e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f3e-114">Requirements</span></span>



| <span data-ttu-id="a8f3e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f3e-115">Requirement</span></span> | <span data-ttu-id="a8f3e-116">Value</span><span class="sxs-lookup"><span data-stu-id="a8f3e-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f3e-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a8f3e-117">Redistributable</span></span><br/> | <span data-ttu-id="a8f3e-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8f3e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a8f3e-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8f3e-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="a8f3e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f3e-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f3e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f3e-122">**Sectores públicos**</span><span class="sxs-lookup"><span data-stu-id="a8f3e-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




