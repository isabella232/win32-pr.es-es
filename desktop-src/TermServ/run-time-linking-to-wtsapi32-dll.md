---
title: Run-Time vincular a Wtsapi32.dll
description: La aplicación puede usar la API de Servicios de Escritorio remoto para vincular dinámicamente al Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la función LoadLibrary para cargar Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421107"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="c6bee-104">Run-Time vincular a Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c6bee-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="c6bee-105">Si la aplicación se ejecuta en un entorno que no es un Servicios de Escritorio remoto entorno, pero desea que la aplicación proporcione funcionalidad adicional cuando se ejecuta en un entorno de Servicios de Escritorio remoto, la aplicación puede usar la API de Servicios de Escritorio remoto para implementar la funcionalidad adicional y vincular dinámicamente a la Wtsapi32.dll en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c6bee-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="c6bee-106">Para ello, la aplicación debe llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="c6bee-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="c6bee-107">Si se produce un error en la llamada **LoadLibrary** , la aplicación se puede ejecutar utilizando su funcionalidad básica.</span><span class="sxs-lookup"><span data-stu-id="c6bee-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="c6bee-108">Si **LoadLibrary** se ejecuta correctamente, la aplicación puede llamar a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar punteros a las funciones servicios de escritorio remoto a las que desea llamar.</span><span class="sxs-lookup"><span data-stu-id="c6bee-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="c6bee-109">Si la aplicación está destinada solo a un entorno de Servicios de Escritorio remoto, la vinculación dinámica no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="c6bee-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="c6bee-110">En este caso, puede incluir Wtsapi32. h y vincular con Wtsapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="c6bee-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="c6bee-111">Después, si la aplicación se inicia en un entorno que no sea Servicios de Escritorio remoto, se cerrará porque Wtsapi32.dll no está presente.</span><span class="sxs-lookup"><span data-stu-id="c6bee-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="c6bee-112">Para obtener información acerca de cómo determinar si la aplicación se ejecuta en un entorno de Servicios de Escritorio remoto, consulte [detectar el entorno de servicios de escritorio remoto](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c6bee-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6bee-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6bee-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6bee-114">Instrucciones generales de programación</span><span class="sxs-lookup"><span data-stu-id="c6bee-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 