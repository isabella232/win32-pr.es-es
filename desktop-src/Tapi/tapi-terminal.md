---
description: La clase de dispositivo TAPI/terminal consta de los dispositivos telefónicos asociados a cada terminal en una línea o el terminal en cada línea asociada a un dispositivo de teléfono. Puede tener acceso a estos dispositivos mediante las funciones dispositivo de línea TAPI o dispositivo de teléfono.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678168"
---
# <a name="tapiterminal"></a><span data-ttu-id="d4847-104">TAPI/terminal</span><span class="sxs-lookup"><span data-stu-id="d4847-104">tapi/terminal</span></span>

<span data-ttu-id="d4847-105">La clase de dispositivo TAPI/terminal consta de los dispositivos telefónicos asociados a cada terminal en una línea o el terminal en cada línea asociada a un dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="d4847-105">The tapi/terminal device class consists of the phone devices associated with each terminal on a line or the terminal on each line associated with a phone device.</span></span> <span data-ttu-id="d4847-106">Puede tener acceso a estos dispositivos mediante las funciones dispositivo de [línea](line-device-functions.md) TAPI o [dispositivo de teléfono](phone-device-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d4847-106">You access these devices by using the TAPI [line device](line-device-functions.md) or [phone device functions](phone-device-functions.md).</span></span>

<span data-ttu-id="d4847-107">La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="d4847-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

<span data-ttu-id="d4847-108">El miembro **adwDeviceId** es una matriz de identificadores de dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="d4847-108">The **adwDeviceId** member is an array of phone device identifiers.</span></span> <span data-ttu-id="d4847-109">Hay un elemento de matriz para cada terminal especificado por el miembro **dwNumTerminals** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="d4847-109">There is one array element for each terminal specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the given line device.</span></span> <span data-ttu-id="d4847-110">Cada elemento especifica el identificador del dispositivo telefónico asociado al terminal correspondiente en la línea.</span><span class="sxs-lookup"><span data-stu-id="d4847-110">Each element specifies the identifier of the phone device associated with the corresponding terminal on the line.</span></span> <span data-ttu-id="d4847-111">Si no hay ningún dispositivo de teléfono asociado a un terminal, el elemento se establece en – 1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="d4847-111">If there is no phone device associated with a terminal, the element is set to –1 (0xFFFFFFFF).</span></span>

<span data-ttu-id="d4847-112">La función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="d4847-112">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

<span data-ttu-id="d4847-113">El miembro **adwTerminalID** es una matriz de identificadores de terminal.</span><span class="sxs-lookup"><span data-stu-id="d4847-113">The **adwTerminalID** member is an array of terminal identifiers.</span></span> <span data-ttu-id="d4847-114">Hay un elemento de matriz para cada identificador de dispositivo de línea especificado por la función [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="d4847-114">There is one array element for each line device identifier specified by the [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) function.</span></span> <span data-ttu-id="d4847-115">Cada elemento de la matriz contiene el identificador de terminal asociado al dispositivo telefónico para el dispositivo de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="d4847-115">Each array element contains the terminal identifier associated with the phone device for the given line device.</span></span> <span data-ttu-id="d4847-116">Si no hay ningún dispositivo de teléfono, el elemento se establece en – 1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="d4847-116">If there is no phone device, the element is set to –1 (0xFFFFFFFF).</span></span> <span data-ttu-id="d4847-117">Los identificadores de terminal van en el valor de cero a uno menos que el número especificado por el miembro **dwNumTerminals** en la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="d4847-117">The terminal identifiers range in value from zero to one less than the number specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>

 

 



