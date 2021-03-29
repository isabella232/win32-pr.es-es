---
description: Agregue todas las propiedades de contraseña de la tabla CustomUserAccounts a la propiedad MsiHiddenProperties de la tabla de propiedades.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Protección de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003134"
---
# <a name="securing-the-installation"></a><span data-ttu-id="a67b0-103">Protección de la instalación</span><span class="sxs-lookup"><span data-stu-id="a67b0-103">Securing the Installation</span></span>

<span data-ttu-id="a67b0-104">Agregue todas las propiedades de contraseña de la tabla CustomUserAccounts a la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="a67b0-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="a67b0-105">Agregue también los nombres de las acciones personalizadas diferidas a la propiedad **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="a67b0-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="a67b0-106">Esto impedirá que el instalador escriba los valores de propiedad confidenciales (las contraseñas) en el registro y garantizará que estos valores no se registran cuando las acciones personalizadas diferidas usan los valores como la propiedad CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="a67b0-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="a67b0-107">Para que la contraseña del usuario esté disponible en el servicio de Windows Installer, la propiedad password debe agregarse a la propiedad [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a67b0-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="a67b0-108">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="a67b0-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="a67b0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a67b0-109">Property</span></span>                                                 | <span data-ttu-id="a67b0-110">Value</span><span class="sxs-lookup"><span data-stu-id="a67b0-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a67b0-111">**MsiHiddenProperties**</span><span class="sxs-lookup"><span data-stu-id="a67b0-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="a67b0-112">TESTUSERPASSWORD; CreateAccount; RemoveAccount RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="a67b0-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="a67b0-113">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="a67b0-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="a67b0-114">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="a67b0-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="a67b0-115">Esto concluye el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a67b0-115">This concludes the sample.</span></span>

 

 



