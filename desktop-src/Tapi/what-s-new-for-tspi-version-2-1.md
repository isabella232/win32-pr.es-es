---
description: A partir de TAPI 2,1, se pueden usar los archivos dll de la interfaz de usuario del proveedor de servicios de telefonía para administrar y mostrar cuadros de diálogo. TAPI carga el archivo DLL en el proceso de una aplicación que invoca cualquiera de las funciones del proveedor de servicios que pueden mostrar un cuadro de diálogo.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Novedades de la versión 2,1 de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678054"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="5e9ab-104">Novedades de la versión 2,1 de TSPI</span><span class="sxs-lookup"><span data-stu-id="5e9ab-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="5e9ab-105">A partir de TAPI 2,1, se pueden usar los archivos dll de la interfaz de usuario del proveedor de servicios de telefonía para administrar y mostrar cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5e9ab-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="5e9ab-106">TAPI carga el archivo DLL en el proceso de una aplicación que invoca cualquiera de las funciones del proveedor de servicios que pueden mostrar un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5e9ab-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="5e9ab-107">A partir de TAPI 2,1, se pueden implementar controladores de solicitudes de proxy.</span><span class="sxs-lookup"><span data-stu-id="5e9ab-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="5e9ab-108">Un controlador es una aplicación de telefonía completa que se ejecuta normalmente en un servidor de telefonía y proporciona servicios que se implementan de forma más adecuada en una aplicación que un controlador.</span><span class="sxs-lookup"><span data-stu-id="5e9ab-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="5e9ab-109">Las funciones y los mensajes que eran nuevos o cambiaron para la versión 2,1 de TSPI son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5e9ab-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="5e9ab-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="5e9ab-111">**TSPI_lineDropNoOwner**:**obsoleto**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="5e9ab-112">**TSPI_lineDropOnClose**:**obsoleto**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="5e9ab-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="5e9ab-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="5e9ab-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="5e9ab-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="5e9ab-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="5e9ab-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="5e9ab-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="5e9ab-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="5e9ab-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="5e9ab-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="5e9ab-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="5e9ab-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="5e9ab-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="5e9ab-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="5e9ab-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e9ab-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="5e9ab-128">La DLL de la interfaz de usuario del proveedor de servicios de telefonía proporciona un medio para permitir la interacción del usuario en el contexto de la aplicación en lugar de en el propio proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="5e9ab-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="5e9ab-129">La versión 2,1 de TSPI proporcionó las siguientes nuevas funciones, mensajes y estructuras para la implementación:</span><span class="sxs-lookup"><span data-stu-id="5e9ab-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="5e9ab-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="5e9ab-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="5e9ab-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="5e9ab-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="5e9ab-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="5e9ab-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="5e9ab-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="5e9ab-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="5e9ab-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="5e9ab-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="5e9ab-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="5e9ab-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="5e9ab-142">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="5e9ab-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="5e9ab-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="5e9ab-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
