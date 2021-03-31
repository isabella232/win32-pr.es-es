---
title: Vincular a la DLL de acceso remoto
description: Si una aplicación se vincula estáticamente al archivo DLL de RASAPI32, la aplicación no se cargará si el servicio de acceso remoto no está instalado.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904734"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="e75d8-103">Vincular a la DLL de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="e75d8-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="e75d8-104">Si una aplicación se vincula estáticamente al archivo DLL de RASAPI32, la aplicación no se cargará si el servicio de acceso remoto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="e75d8-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="e75d8-105">Una aplicación RAS puede cargarse cuando no se instala RAS mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar el archivo dll y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener punteros a las funciones RAS.</span><span class="sxs-lookup"><span data-stu-id="e75d8-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="e75d8-106">Las funciones RAS se encuentran en RASAPI32.DLL.</span><span class="sxs-lookup"><span data-stu-id="e75d8-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="e75d8-107">La biblioteca de importación para estas funciones es RASAPI32. Obj.</span><span class="sxs-lookup"><span data-stu-id="e75d8-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="e75d8-108">Para usar las funciones RAS, los programas deben incluir los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="e75d8-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="e75d8-109">Archivo</span><span class="sxs-lookup"><span data-stu-id="e75d8-109">File</span></span>       | <span data-ttu-id="e75d8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e75d8-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="e75d8-111">Acceso. C</span><span class="sxs-lookup"><span data-stu-id="e75d8-111">RAS.H</span></span>      | <span data-ttu-id="e75d8-112">Contiene los prototipos de función RAS, las constantes y las definiciones de estructura.</span><span class="sxs-lookup"><span data-stu-id="e75d8-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="e75d8-113">RASERROR. C</span><span class="sxs-lookup"><span data-stu-id="e75d8-113">RASERROR.H</span></span> | <span data-ttu-id="e75d8-114">Contiene los códigos de error de RAS.</span><span class="sxs-lookup"><span data-stu-id="e75d8-114">Contains the RAS error codes.</span></span>                                               |



 

 

 