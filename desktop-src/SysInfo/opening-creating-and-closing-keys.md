---
description: Para que una aplicación pueda agregar datos al registro, debe crear o abrir una clave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Abrir, crear y cerrar claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666636"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="85488-103">Abrir, crear y cerrar claves</span><span class="sxs-lookup"><span data-stu-id="85488-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="85488-104">Para que una aplicación pueda agregar datos al registro, debe crear o abrir una clave.</span><span class="sxs-lookup"><span data-stu-id="85488-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="85488-105">Para crear o abrir una clave, una aplicación siempre hace referencia a la clave como una subclave de una clave abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="85488-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="85488-106">Las siguientes claves predefinidas siempre están abiertas **: HKEY \_ local \_ Machine**, **HKEY \_ classes \_ root**, **HKEY \_ users** y **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="85488-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="85488-107">Una aplicación utiliza la función [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) para abrir una clave y la función [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) para crear una clave.</span><span class="sxs-lookup"><span data-stu-id="85488-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="85488-108">Un árbol del registro puede tener un nivel de 512 niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="85488-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="85488-109">Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.</span><span class="sxs-lookup"><span data-stu-id="85488-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="85488-110">Una aplicación puede usar la función [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) para cerrar una clave y escribir los datos que contiene en el registro.</span><span class="sxs-lookup"><span data-stu-id="85488-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="85488-111">**RegCloseKey** no escribe necesariamente los datos en el registro antes de devolver; la memoria caché puede tardar hasta varios segundos en vaciarse en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="85488-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="85488-112">Si una aplicación debe escribir explícitamente los datos del registro en el disco duro, puede usar la función [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) .</span><span class="sxs-lookup"><span data-stu-id="85488-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="85488-113">Sin embargo, **RegFlushKey** utiliza muchos recursos del sistema y solo se debe llamar cuando sea absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="85488-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



