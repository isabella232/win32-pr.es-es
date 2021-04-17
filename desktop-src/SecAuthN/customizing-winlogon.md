---
description: Personalizar el comportamiento de Winlogon implementando un proveedor de credenciales.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalización de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648223"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="0f007-103">Personalización de Winlogon</span><span class="sxs-lookup"><span data-stu-id="0f007-103">Customizing Winlogon</span></span>

<span data-ttu-id="0f007-104">Personalizar el comportamiento de [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando un proveedor de credenciales.</span><span class="sxs-lookup"><span data-stu-id="0f007-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="0f007-105">Para obtener información sobre los proveedores de credenciales, consulte [**ICredentialProvider (interfaz**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider)).</span><span class="sxs-lookup"><span data-stu-id="0f007-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="0f007-106">**Windows Server 2003 y Windows XP:** No se admiten proveedores de credenciales.</span><span class="sxs-lookup"><span data-stu-id="0f007-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="0f007-107">En las secciones siguientes se describen las distintas formas de personalizar Winlogon en versiones de Windows anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0f007-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="0f007-108">Los paquetes dll de GINA y de notificación de Winlogon se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0f007-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="0f007-109">Paquetes de notificación de Winlogon</span><span class="sxs-lookup"><span data-stu-id="0f007-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="0f007-110">Código auxiliar de GINA</span><span class="sxs-lookup"><span data-stu-id="0f007-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="0f007-111">Enlaces de GINA</span><span class="sxs-lookup"><span data-stu-id="0f007-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="0f007-112">Paquetes de notificación de Winlogon</span><span class="sxs-lookup"><span data-stu-id="0f007-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="0f007-113">Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="0f007-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="0f007-114">Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a cada paquete de notificación para proporcionar información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="0f007-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="0f007-115">Para obtener más información, consulte [paquetes de notificación de Winlogon](winlogon-notification-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0f007-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="0f007-116">Código auxiliar de GINA</span><span class="sxs-lookup"><span data-stu-id="0f007-116">GINA Stubs</span></span>

<span data-ttu-id="0f007-117">Un código auxiliar de [*Gina*](/windows/desktop/SecGloss/g-gly) es un archivo dll de Gina personalizado que usa las implementaciones de la función de exportación de un archivo dll de Gina instalado previamente (normalmente MsGina.dll).</span><span class="sxs-lookup"><span data-stu-id="0f007-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="0f007-118">Un código auxiliar GINA obtiene punteros a cada una de las funciones exportadas por el archivo DLL de GINA instalado previamente.</span><span class="sxs-lookup"><span data-stu-id="0f007-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="0f007-119">Cada función de código auxiliar de GINA usa el puntero de función adecuado para llamar a la función correspondiente en el archivo DLL de GINA instalado previamente.</span><span class="sxs-lookup"><span data-stu-id="0f007-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f007-120">Cada función de código auxiliar de GINA debe llamar a la función correspondiente en el GINA instalado previamente.</span><span class="sxs-lookup"><span data-stu-id="0f007-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="0f007-121">Una función de código auxiliar GINA puede implementar funcionalidad adicional en una o varias de sus funciones de exportación.</span><span class="sxs-lookup"><span data-stu-id="0f007-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="0f007-122">Por ejemplo, la función [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) de un código auxiliar de Gina podría comprobar la hora actual antes de llamar a la función **WlxLoggedOutSAS** del MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="0f007-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="0f007-123">Si la hora actual estaba dentro de un intervalo específico, la función de código auxiliar podría mostrar un mensaje que indica que no se permite el inicio de sesión durante ese período de tiempo y devolver **WLX \_ SAS \_ Action \_ None** a Winlogon.</span><span class="sxs-lookup"><span data-stu-id="0f007-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="0f007-124">A continuación, se llamará a la función **WlxLoggedOutSAS** del MsGina.dll solo durante el período de tiempo permitido.</span><span class="sxs-lookup"><span data-stu-id="0f007-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="0f007-125">La aplicación de código auxiliar de GINA obtiene una tabla de envío para que las funciones de Winlogon admitan las funciones mediante el parámetro *pWinlogonFunctions* de la función [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) .</span><span class="sxs-lookup"><span data-stu-id="0f007-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="0f007-126">La aplicación de código auxiliar de GINA puede utilizar esta tabla de envío para llamar a las funciones de compatibilidad de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="0f007-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="0f007-127">Por ejemplo, una aplicación de código auxiliar de GINA puede llamar a la función [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) para que se produzca un evento de [*secuencia de atención segura*](/windows/desktop/SecGloss/s-gly) (SAS) cuando se inserta una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) en un [*lector*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="0f007-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="0f007-128">Para obtener más información sobre cómo crear un código auxiliar de GINA, vea el ejemplo de código auxiliar de Gina en el \\ \\ \\ \\ directorio Gina GinaStub Security de la instalación del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0f007-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="0f007-129">Todas las llamadas entre GINA y Winlogon deben estar dentro de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="0f007-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="0f007-130">Enlaces de GINA</span><span class="sxs-lookup"><span data-stu-id="0f007-130">GINA Hooks</span></span>

<span data-ttu-id="0f007-131">Un enlace GINA es un código auxiliar de GINA que, en su implementación de la función [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , reemplaza el puntero a la función [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support en la tabla Dispatch con un puntero a su propia implementación de la función **WlxDialogBoxParam** .</span><span class="sxs-lookup"><span data-stu-id="0f007-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="0f007-132">Como resultado, cada vez que el GINA instalado previamente (normalmente MsGina.dll) llama a la función **WlxDialogBoxParam** , se llama a la función implementada por el enlace gina.</span><span class="sxs-lookup"><span data-stu-id="0f007-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="0f007-133">La función [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) que implementa el enlace Gina puede reemplazar el procedimiento de devolución de llamada [**función dialogproc**](/windows/win32/api/winuser/nc-winuser-dlgproc) que responde a un evento de cuadro de diálogo específico.</span><span class="sxs-lookup"><span data-stu-id="0f007-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="0f007-134">Esto proporciona al enlace de GINA control total sobre la apariencia y el comportamiento de todos los cuadros de diálogo que crea MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="0f007-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="0f007-135">Para obtener más información sobre cómo crear un enlace GINA, consulte el ejemplo de enlaces de Gina en el \\ \\ \\ \\ Directorio de ejemplos de GinaHook de seguridad de la instalación de un SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0f007-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="0f007-136">Todas las llamadas entre GINA y Winlogon deben estar dentro de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="0f007-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
