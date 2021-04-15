---
description: Indica un tipo de cambio de estado de servicio para la supervisión y la generación de informes.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Enumeración SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669723"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="77ca5-103">\_Enumeración de tipo de evento SC \_</span><span class="sxs-lookup"><span data-stu-id="77ca5-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="77ca5-104">Indica un tipo de cambio de estado de servicio para la supervisión y la generación de informes.</span><span class="sxs-lookup"><span data-stu-id="77ca5-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ca5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77ca5-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="77ca5-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="77ca5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="77ca5-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**cambio en la \_ base de datos de eventos SC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77ca5-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="77ca5-108">Se ha agregado o eliminado un servicio.</span><span class="sxs-lookup"><span data-stu-id="77ca5-108">A service has been added or deleted.</span></span> <span data-ttu-id="77ca5-109">El parámetro *hService* de la función [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) debe ser un identificador del SCM.</span><span class="sxs-lookup"><span data-stu-id="77ca5-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="77ca5-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_cambio de \_ propiedad de evento de SC \_**</span><span class="sxs-lookup"><span data-stu-id="77ca5-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="77ca5-111">Se han actualizado una o varias propiedades de servicio.</span><span class="sxs-lookup"><span data-stu-id="77ca5-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="77ca5-112">El parámetro *hService* de la función [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) debe ser un identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="77ca5-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="77ca5-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_cambio de \_ Estado de evento de SC \_**</span><span class="sxs-lookup"><span data-stu-id="77ca5-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="77ca5-114">El estado de un servicio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="77ca5-114">The status of a service has changed.</span></span> <span data-ttu-id="77ca5-115">El parámetro *hService* de la función [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) debe ser un identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="77ca5-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77ca5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ca5-116">Requirements</span></span>



| <span data-ttu-id="77ca5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ca5-117">Requirement</span></span> | <span data-ttu-id="77ca5-118">Value</span><span class="sxs-lookup"><span data-stu-id="77ca5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77ca5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77ca5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77ca5-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="77ca5-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="77ca5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77ca5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77ca5-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77ca5-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="77ca5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77ca5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77ca5-124"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77ca5-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




