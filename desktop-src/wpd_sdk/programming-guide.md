---
title: Guía de programación de WPD
description: Guía de programación
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f774ffd9d7576a07b34c467a5a155d98e4f3e703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697652"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="27fcf-103">Guía de programación de WPD</span><span class="sxs-lookup"><span data-stu-id="27fcf-103">WPD programming guide</span></span>

<span data-ttu-id="27fcf-104">El origen principal de esta guía de programación es un ejemplo que se incluye con el kit de desarrollo de software (SDK) de dispositivos portátiles de Windows (WPD).</span><span class="sxs-lookup"><span data-stu-id="27fcf-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="27fcf-105">Este ejemplo, denominado WpdApiSample.exe, consta de siete módulos. cpp.</span><span class="sxs-lookup"><span data-stu-id="27fcf-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="27fcf-106">Seis de estos módulos contienen el código que muestra 26 tareas que una aplicación puede realizar mediante la interfaz de programación de aplicaciones (API) de WPD.</span><span class="sxs-lookup"><span data-stu-id="27fcf-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="27fcf-107">Las excepciones a lo anterior son los temas que describen: tareas del servicio de dispositivo, las extensiones del menú contextual y de la hoja de propiedades. estos temas no se han tomado de WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="27fcf-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="27fcf-108">Las tareas del servicio de dispositivo se basan en el ejemplo denominado WpdServiceApiSample.</span><span class="sxs-lookup"><span data-stu-id="27fcf-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="27fcf-109">Las extensiones del menú contextual y de la hoja de propiedades son fragmentos de código procedentes de aplicaciones que no se distribuyen con el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="27fcf-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="27fcf-110">Las siguientes secciones se centran en las tareas que se realizan en estos ejemplos y explican cómo se realiza cada una de ellas con las interfaces de WPD y varios métodos que se encuentran en estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="27fcf-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27fcf-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27fcf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27fcf-112">**Dispositivos portátiles de Windows**</span><span class="sxs-lookup"><span data-stu-id="27fcf-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
