---
description: Un usuario puede especificar la configuración de documento predeterminada para una impresora. Esto se denomina DEVMODE por usuario, ya que solo afecta a los valores predeterminados de un usuario determinado, y la información de cada impresora se define en una estructura DEVMODE independiente.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706303"
---
# <a name="per-user-devmode"></a><span data-ttu-id="1db3c-104">Per-User DEVMODE</span><span class="sxs-lookup"><span data-stu-id="1db3c-104">Per-User DEVMODE</span></span>

<span data-ttu-id="1db3c-105">Un usuario puede especificar la configuración de documento predeterminada para una impresora.</span><span class="sxs-lookup"><span data-stu-id="1db3c-105">A user can specify the default document settings for a printer.</span></span> <span data-ttu-id="1db3c-106">Esto se denomina *DEVMODE por usuario* , ya que solo afecta a los valores predeterminados de un usuario determinado, y la información de cada impresora se define en una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) independiente.</span><span class="sxs-lookup"><span data-stu-id="1db3c-106">This is called the *per-user DEVMODE* because it only affects the defaults for a particular user, and the information for each printer is defined in a separate [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

<span data-ttu-id="1db3c-107">Para establecer el DEVMODE por usuario, llame a [**SetPrinter**](setprinter.md) con la información de la [**impresora \_ \_ 2**](printer-info-2.md) o la estructura de la [**\_ información \_**](printer-info-9.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1db3c-107">To set the per-user DEVMODE, call [**SetPrinter**](setprinter.md) with either the [**PRINTER\_INFO\_2**](printer-info-2.md) or the [**PRINTER\_INFO\_9**](printer-info-9.md) structure.</span></span> <span data-ttu-id="1db3c-108">Para restablecer el DEVMODE por usuario en el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)global predeterminado, llame a **SetPrinter** con la estructura de la información de la [**impresora \_ \_ 8**](printer-info-8.md) .</span><span class="sxs-lookup"><span data-stu-id="1db3c-108">To reset the per-user DEVMODE to the global default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), call **SetPrinter** with the [**PRINTER\_INFO\_8**](printer-info-8.md) structure.</span></span>

 

 



