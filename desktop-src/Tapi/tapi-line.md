---
description: La clase de dispositivo TAPI/línea consta de todos los dispositivos de línea. Puede tener acceso a estos dispositivos con las funciones de línea TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678234"
---
# <a name="tapiline"></a><span data-ttu-id="20971-104">TAPI/línea</span><span class="sxs-lookup"><span data-stu-id="20971-104">tapi/line</span></span>

<span data-ttu-id="20971-105">La clase de dispositivo TAPI/línea consta de todos los dispositivos de línea.</span><span class="sxs-lookup"><span data-stu-id="20971-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="20971-106">Puede tener acceso a estos dispositivos con las funciones de línea TAPI.</span><span class="sxs-lookup"><span data-stu-id="20971-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="20971-107">La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional.</span><span class="sxs-lookup"><span data-stu-id="20971-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="20971-108">El miembro **dwDeviceId** es el identificador del dispositivo de línea asociado al identificador de línea proporcionado por [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="20971-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="20971-109">La función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) también rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo **DWSTRINGFORMAT** en \_ el binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="20971-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="20971-110">El miembro **adwDeviceIds** es una matriz que contiene los identificadores de dispositivos de todos los dispositivos de línea asociados al dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="20971-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="20971-111">Si no hay dispositivos de línea asociados, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) devuelve el valor de INVALDEVICECLASS de PHONEERR \_ .</span><span class="sxs-lookup"><span data-stu-id="20971-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 



