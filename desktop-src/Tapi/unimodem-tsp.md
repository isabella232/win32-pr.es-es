---
description: El Unimodem, o controlador de módem universal, TSP (Unimdm. TSP) proporciona acceso a casi todos los módems estándar.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: TSP de Unimodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688318"
---
# <a name="unimodem-tsp"></a><span data-ttu-id="e2cd9-103">TSP de Unimodem</span><span class="sxs-lookup"><span data-stu-id="e2cd9-103">Unimodem TSP</span></span>

<span data-ttu-id="e2cd9-104">El Unimodem, o controlador de módem universal, TSP (Unimdm. TSP) proporciona acceso a casi todos los módems estándar.</span><span class="sxs-lookup"><span data-stu-id="e2cd9-104">The Unimodem, or Universal Modem Driver, TSP (Unimdm.tsp) provides access to nearly all standard modems.</span></span> <span data-ttu-id="e2cd9-105">Admite módems de voz que permiten el streaming dúplex medio.</span><span class="sxs-lookup"><span data-stu-id="e2cd9-105">It supports voice modems that allow half-duplex streaming.</span></span> <span data-ttu-id="e2cd9-106">Son compatibles con Wave MSP y el control de flujo es posible.</span><span class="sxs-lookup"><span data-stu-id="e2cd9-106">They are supported by the Wave MSP and stream control is possible.</span></span> <span data-ttu-id="e2cd9-107">(Tenga en cuenta que Unimodem en Windows NT 4,0 o versiones anteriores no es compatible con los módems de voz, por lo que no es posible el control de flujo directo).</span><span class="sxs-lookup"><span data-stu-id="e2cd9-107">(Note that Unimodem on Windows NT 4.0 or earlier does not support voice modems, so direct stream control is not possible.)</span></span>

<span data-ttu-id="e2cd9-108">Este TSP admite un valor de [**tipo de dirección**](./lineaddresstype--constants.md) de LINEADDRESSTYPE \_ PHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="e2cd9-108">This TSP supports an [**address type**](./lineaddresstype--constants.md) value of LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="e2cd9-109">Si el programador desea usar las reglas de marcado, la interfaz [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) de TAPI 3 o la función [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) de TAPI 2 deben usarse para obtener una cadena de marcado desde un número de teléfono en formato canónico.</span><span class="sxs-lookup"><span data-stu-id="e2cd9-109">If the programmer wants to use the dialing rules, the TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) interface or the TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) function must be used to obtain a dialable string from a phone number in canonical format.</span></span>

<span data-ttu-id="e2cd9-110">El TSP de Unimodem se instala con los sistemas operativos Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 y Windows 95.</span><span class="sxs-lookup"><span data-stu-id="e2cd9-110">The Unimodem TSP is installed with Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98, and Windows 95.</span></span>

 

 
