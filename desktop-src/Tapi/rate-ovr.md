---
description: La velocidad o el ancho de banda de una llamada especifica la velocidad de transmisión de datos. Tres puntos de datos identifican la velocidad actual de la velocidad máxima de un modo de portador especificado y la tasa mínima del modo de portador.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarifa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678237"
---
# <a name="rate"></a><span data-ttu-id="a7455-104">Tarifa</span><span class="sxs-lookup"><span data-stu-id="a7455-104">Rate</span></span>

<span data-ttu-id="a7455-105">La velocidad (o ancho de banda) de una llamada especifica la velocidad de transmisión de datos.</span><span class="sxs-lookup"><span data-stu-id="a7455-105">The rate (or bandwidth) of a call specifies the speed of data transmission.</span></span> <span data-ttu-id="a7455-106">Frecuencia de identificación de tres puntos de datos: la velocidad actual, la velocidad máxima de un modo de portador especificado y la tasa mínima del modo de portador.</span><span class="sxs-lookup"><span data-stu-id="a7455-106">Three data points identify rate: the current rate, the maximum rate for a specified bearer mode, and the minimum rate for the bearer mode.</span></span>

<span data-ttu-id="a7455-107">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="a7455-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="a7455-108">\* \* TAPI 2. x: \* \*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** o **dwMaxRate** miembro de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="a7455-108">\*\*TAPI 2.x:  \*\*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwMinRate** or **dwMaxRate** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="a7455-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** o **CIL \_ Rate** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="a7455-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_MAXRATE**, **CIL\_MINRATE**, or **CIL\_RATE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

<span data-ttu-id="a7455-110">\* \* TSPI: \* \*[**line \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) Message, con *dwParam1* establecido en LINECALLINFOSTATE \_ Rate</span><span class="sxs-lookup"><span data-stu-id="a7455-110">\*\*TSPI:  \*\*[**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_RATE</span></span>

 

 
