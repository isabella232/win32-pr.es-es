---
description: El servicio Windows Installer usa el idioma del usuario actual en todos los cuadros de diálogo hasta que se abre un paquete de Windows Installer.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localizar el idioma que se muestra en los cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687823"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="8d479-103">Localizar el idioma que se muestra en los cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="8d479-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="8d479-104">El servicio Windows Installer usa el idioma del usuario actual en todos los cuadros de diálogo hasta que se abre un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8d479-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="8d479-105">El Windows Installer determina esto mediante **GetUserDefaultUILanguage**.</span><span class="sxs-lookup"><span data-stu-id="8d479-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="8d479-106">Cuando se abre un paquete de Windows Installer, el instalador muestra los cuadros de diálogo con el idioma del paquete tal y como se especifica en la propiedad de Resumen de la [**plantilla**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="8d479-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="8d479-107">Para obtener más información sobre cómo localizar el idioma de un paquete de Windows Installer, vea también [un ejemplo de localización](a-localization-example.md).</span><span class="sxs-lookup"><span data-stu-id="8d479-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 



