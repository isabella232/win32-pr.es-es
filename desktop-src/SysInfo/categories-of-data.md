---
description: 'Antes de colocar los datos en el registro, una aplicación debe dividir los datos en dos categorías: datos específicos del equipo y datos específicos del usuario.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorías de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669981"
---
# <a name="categories-of-data"></a><span data-ttu-id="41df5-103">Categorías de datos</span><span class="sxs-lookup"><span data-stu-id="41df5-103">Categories of Data</span></span>

<span data-ttu-id="41df5-104">Antes de colocar los datos en el registro, una aplicación debe dividir los datos en dos categorías: datos específicos del equipo y datos específicos del usuario.</span><span class="sxs-lookup"><span data-stu-id="41df5-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="41df5-105">Al hacer esta distinción, una aplicación puede admitir varios usuarios y ubicar datos específicos del usuario en una red y usar esos datos en ubicaciones diferentes, lo que permite datos de Perfil de usuario independientes de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="41df5-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="41df5-106">(Un perfil de usuario es un conjunto de datos de configuración que se guarda para cada usuario).</span><span class="sxs-lookup"><span data-stu-id="41df5-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="41df5-107">Cuando se instala la aplicación, debe registrar los datos específicos del equipo en la clave **del \_ \_ equipo local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="41df5-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="41df5-108">En concreto, debe crear claves para el nombre de la compañía, el nombre del producto y el número de versión, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="41df5-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="41df5-109">**HKEY \_ \_ \\ Software \\ de máquina local**_MyCompany \\ \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="41df5-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="41df5-110">Si la aplicación admite COM, debe registrar esos datos en **\_ \_ \\ \\ las clases de software de máquina local HKEY**.</span><span class="sxs-lookup"><span data-stu-id="41df5-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="41df5-111">Una aplicación debe registrar datos específicos del usuario en la clave del **\_ \_ usuario actual HKEY** , tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="41df5-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="41df5-112">**HKEY \_ \_ \\ Software \\ de usuario actual**, mi _\\ producto \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="41df5-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



