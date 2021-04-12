---
title: Comprobación de automatización de la interfaz de usuario (comprobar UIA)
description: La comprobación de la automatización de la interfaz de usuario (UIA Verify) es un marco de pruebas para pruebas manuales y automatizadas de la implementación de una aplicación o un control de la automatización de la interfaz de usuario de Microsoft.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- UI Automation Verify
- Comprobar UIA
- Implementación de automatización de la interfaz de usuario, prueba
- probar la automatización de la interfaz de usuario
- Herramientas de prueba de UIA
- Herramientas de pruebas de UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420349"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="2fe50-109">Herramientas de accesibilidad: comprobación de UI Automation (UIA Verify)</span><span class="sxs-lookup"><span data-stu-id="2fe50-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="2fe50-110">La comprobación de la automatización de la **interfaz de usuario (UIA Verify)** es un marco de pruebas para pruebas manuales y automatizadas de la implementación de una aplicación o un control de la automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2fe50-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="2fe50-111">La mayor parte de la funcionalidad del marco de pruebas procede de un archivo DLL denominado WUIATestLibrary.dll.</span><span class="sxs-lookup"><span data-stu-id="2fe50-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="2fe50-112">Este archivo DLL contiene el código para probar la funcionalidad de automatización de la interfaz de usuario específica y también admite el registro de los resultados de pruebas.</span><span class="sxs-lookup"><span data-stu-id="2fe50-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="2fe50-113">Puede integrar la aplicación en el código de prueba y realizar comprobaciones regulares y automatizadas de los escenarios de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2fe50-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="2fe50-114">**UIA Verify** se instala con el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2fe50-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2fe50-115">Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform* > \\ UIAVerify de la ruta de instalación de SDK (VisualUIAVerifyNative.exe).</span><span class="sxs-lookup"><span data-stu-id="2fe50-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="2fe50-116">**UIA Verify** consta de una API denominada Biblioteca de pruebas de automatización de la interfaz de usuario y una interfaz de GUI denominada visual **UI Automation Verify**.</span><span class="sxs-lookup"><span data-stu-id="2fe50-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="2fe50-117">Se describen en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2fe50-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="2fe50-118">La comprobación de automatización de la **interfaz de usuario** es una herramienta heredada.</span><span class="sxs-lookup"><span data-stu-id="2fe50-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="2fe50-119">En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="2fe50-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe50-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fe50-120">Requirements</span></span>

<span data-ttu-id="2fe50-121">La automatización de la interfaz de usuario debe estar presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2fe50-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="2fe50-122">Para obtener más información, vea la sección "requirements" de automatización de la [interfaz de usuario](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="2fe50-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="2fe50-123">**UIA Verify** se instala como parte del conjunto general de herramientas en el Windows SDK, no se distribuye como una descarga independiente.</span><span class="sxs-lookup"><span data-stu-id="2fe50-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="2fe50-124">El Windows SDK incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección.</span><span class="sxs-lookup"><span data-stu-id="2fe50-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="2fe50-125">Obtiene el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2fe50-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="2fe50-126">(También hay un archivo de descarga de SDK vinculado desde esa página, si necesita una versión anterior).</span><span class="sxs-lookup"><span data-stu-id="2fe50-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="2fe50-127">Para ejecutar **UIA Verify** como una herramienta visual, busque VisualUIAVerifyNative.exe en la \\ carpeta bin UIAVerify de la \\ < *plataforma* > \\ y ejecútelo (normalmente no tiene que ejecutarse como administrador).</span><span class="sxs-lookup"><span data-stu-id="2fe50-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="2fe50-128">Para obtener más información, consulte Comprobación de la automatización de la [interfaz de usuario visual](visual-ui-automation-verify.md).</span><span class="sxs-lookup"><span data-stu-id="2fe50-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="2fe50-129">Para usar las bibliotecas, vea [UI Automation test Library](ui-automation-test-library.md).</span><span class="sxs-lookup"><span data-stu-id="2fe50-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fe50-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fe50-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe50-131">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="2fe50-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="2fe50-132">Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="2fe50-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="2fe50-133">Herramientas de pruebas</span><span class="sxs-lookup"><span data-stu-id="2fe50-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="2fe50-134">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="2fe50-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




