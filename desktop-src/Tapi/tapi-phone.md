---
description: La clase de dispositivo TAPI/teléfono se compone de todos los dispositivos telefónicos. Puede tener acceso a estos dispositivos mediante las funciones de teléfono de TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002444"
---
# <a name="tapiphone"></a><span data-ttu-id="b04b6-104">TAPI/teléfono</span><span class="sxs-lookup"><span data-stu-id="b04b6-104">tapi/phone</span></span>

<span data-ttu-id="b04b6-105">La clase de dispositivo TAPI/teléfono se compone de todos los dispositivos telefónicos.</span><span class="sxs-lookup"><span data-stu-id="b04b6-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="b04b6-106">Puede tener acceso a estos dispositivos mediante las funciones de teléfono de TAPI.</span><span class="sxs-lookup"><span data-stu-id="b04b6-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="b04b6-107">La función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="b04b6-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="b04b6-108">El miembro **dwDeviceId** es el identificador del dispositivo telefónico asociado al identificador de teléfono proporcionado por [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="b04b6-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="b04b6-109">La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) también rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo **DWSTRINGFORMAT** en \_ el binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="b04b6-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="b04b6-110">El miembro **adwDeviceIds** es una matriz que contiene los identificadores de dispositivos de todos los dispositivos telefónicos asociados con el dispositivo de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="b04b6-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="b04b6-111">Si no hay ningún dispositivo telefónico asociado, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) devuelve el \_ valor INVALDEVICECLASS de LINEERR.</span><span class="sxs-lookup"><span data-stu-id="b04b6-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 



