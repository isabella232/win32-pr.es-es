---
description: Convierte la hora universal coordinada (hora del meridiano de Greenwich) en la hora local del equipo.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Utilities. UTCTimeToLocalTime (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689907"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="0bcc4-103">Utilities. UTCTimeToLocalTime (método)</span><span class="sxs-lookup"><span data-stu-id="0bcc4-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="0bcc4-104">\[El método **UTCTimeToLocalTime** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="0bcc4-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="0bcc4-105">El método **UTCTimeToLocalTime** convierte la hora universal coordinada (hora del meridiano de Greenwich) en la hora local del equipo.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcc4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bcc4-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="0bcc4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bcc4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bcc4-108">*UTCTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bcc4-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bcc4-109">Hora universal coordinada que se va a convertir en la hora local del equipo.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bcc4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bcc4-110">Return value</span></span>

<span data-ttu-id="0bcc4-111">La hora local que corresponde a la hora universal coordinada especificada.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcc4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bcc4-112">Remarks</span></span>

<span data-ttu-id="0bcc4-113">Aunque el sistema utiliza la hora universal coordinada internamente, las aplicaciones suelen mostrar la hora local, que es la fecha y la hora del día de la zona horaria local del equipo.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcc4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bcc4-114">Requirements</span></span>



| <span data-ttu-id="0bcc4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bcc4-115">Requirement</span></span> | <span data-ttu-id="0bcc4-116">Value</span><span class="sxs-lookup"><span data-stu-id="0bcc4-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcc4-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0bcc4-117">Redistributable</span></span><br/> | <span data-ttu-id="0bcc4-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0bcc4-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0bcc4-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0bcc4-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="0bcc4-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bcc4-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bcc4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bcc4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcc4-122">**Sectores públicos**</span><span class="sxs-lookup"><span data-stu-id="0bcc4-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




