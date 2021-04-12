---
description: Cada identificador de idioma se compone de un identificador de idioma principal que indica el idioma y un identificador de idioma que indica el país o región.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes y cadenas de identificador de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360807"
---
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="b6ed4-103">Constantes y cadenas de identificador de idioma</span><span class="sxs-lookup"><span data-stu-id="b6ed4-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6ed4-104">Las constantes de identificador de idioma están desusadas y no se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="b6ed4-105">Siempre se prefiere el uso de nombres de configuración regional en lugar de los identificadores de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="b6ed4-106">Vea [identificador de idioma](language-identifiers.md) para obtener una descripción de los identificadores de idioma.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="b6ed4-107">Un identificador principal o de subidioma puede estar definido por el usuario o ser predefinido.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="b6ed4-108">Para los identificadores de idioma principal predefinidos con sus identificadores de subidioma válidos, vea [[ms-LCID]: referencia de identificador de idioma de Windows (LCID)](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span><span class="sxs-lookup"><span data-stu-id="b6ed4-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="b6ed4-109">Si no hay ningún identificador de subidioma para usar con un identificador de idioma principal, la aplicación debe usar el **\_ valor predeterminado de sublang**.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="b6ed4-110">Debe usar el **sublang \_ neutro** para los recursos que son iguales para todos los subidiomas de un idioma principal.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="b6ed4-111">Un identificador de idioma principal definido por el usuario tiene un valor en el intervalo de 0x0200 a 0x03ff.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="b6ed4-112">Todos los demás valores están reservados para el uso del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="b6ed4-113">Un identificador de subidioma definido por el usuario tiene un valor en el intervalo de 0x20 a 0x3F.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="b6ed4-114">Todos los demás valores están reservados para el uso del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b6ed4-114">All other values are reserved for operating system use.</span></span>
