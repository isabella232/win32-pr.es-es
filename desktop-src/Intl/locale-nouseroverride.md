---
description: configuración regional \_ NOUSEROVERRIDE
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652701"
---
# <a name="locale_nouseroverride"></a><span data-ttu-id="10b1b-103">configuración regional \_ NOUSEROVERRIDE</span><span class="sxs-lookup"><span data-stu-id="10b1b-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="10b1b-104">Dado que la configuración regional \_ NOUSEROVERRIDE deshabilita las preferencias del usuario, se desaconseja su uso.</span><span class="sxs-lookup"><span data-stu-id="10b1b-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="10b1b-105">Esta constante no garantiza la estabilidad de los datos, ya que las [configuraciones regionales personalizadas](custom-locales.md), las actualizaciones del servicio, las distintas versiones del sistema operativo y otros escenarios pueden cambiar los datos de maneras inesperadas.</span><span class="sxs-lookup"><span data-stu-id="10b1b-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="10b1b-106">Para obtener más información, consulte [uso de datos de configuración regional persistentes](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="10b1b-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="10b1b-107">No se invalida el usuario.</span><span class="sxs-lookup"><span data-stu-id="10b1b-107">No user override.</span></span> <span data-ttu-id="10b1b-108">En varias funciones, por ejemplo, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), esta constante hace que la función omita cualquier invalidación de usuario y use el valor predeterminado del sistema para cualquier otra constante especificada en la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="10b1b-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="10b1b-109">La información se recupera de la base de datos de configuración regional, incluso si el identificador indica la configuración regional actual y el usuario ha cambiado algunos de los valores mediante el panel de control, o si una aplicación ha cambiado estos valores mediante [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="10b1b-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="10b1b-110">Si no se especifica esta constante, los valores que el usuario haya configurado desde el panel de control o que una aplicación haya configurado con [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) tienen prioridad sobre la configuración de la base de datos para la configuración regional predeterminada del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="10b1b-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



