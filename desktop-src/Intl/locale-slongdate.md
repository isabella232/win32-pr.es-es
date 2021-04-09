---
description: configuración regional \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154532"
---
# <a name="locale_slongdate"></a><span data-ttu-id="ce3ce-103">configuración regional \_ SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="ce3ce-103">LOCALE\_SLONGDATE</span></span>

<span data-ttu-id="ce3ce-104">Cadena de formato de fecha larga para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-104">Long date formatting string for the locale.</span></span> <span data-ttu-id="ce3ce-105">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="ce3ce-106">La cadena puede constar de una combinación de [imágenes con formato de día, mes, año y era](day--month--year--and-era-format-pictures.md) y cualquier cadena de caracteres entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md) and any string of characters enclosed in single quotes.</span></span> <span data-ttu-id="ce3ce-107">Los caracteres entre comillas simples permanecen como se especificó.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-107">Characters in single quotes remain as specified.</span></span> <span data-ttu-id="ce3ce-108">Por ejemplo, la fecha larga española (España) es "dddd, DD ' de ' MMMM ' de ' YYYY".</span><span class="sxs-lookup"><span data-stu-id="ce3ce-108">For example, the Spanish (Spain) long date is "dddd, dd' de 'MMMM' de 'yyyy".</span></span> <span data-ttu-id="ce3ce-109">Las configuraciones regionales pueden definir varios formatos de fecha larga.</span><span class="sxs-lookup"><span data-stu-id="ce3ce-109">Locales can define multiple long date formats.</span></span>

<span data-ttu-id="ce3ce-110">Para obtener todos los formatos de fecha larga de una configuración regional, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)o [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="ce3ce-110">To get all of the long date formats for a locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



