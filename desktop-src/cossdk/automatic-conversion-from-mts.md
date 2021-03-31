---
description: Conversión automática desde MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversión automática desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153270"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="91538-103">Conversión automática desde MTS</span><span class="sxs-lookup"><span data-stu-id="91538-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="91538-104">La conversión automática se produce en dos pasos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="91538-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="91538-105">Durante la instalación de Windows.</span><span class="sxs-lookup"><span data-stu-id="91538-105">During Windows setup.</span></span> <span data-ttu-id="91538-106">El proceso de instalación de Windows controla la conversión a través de la utilidad MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="91538-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="91538-107">Si se produce un error en el paso 1, es posible que algunos o todos los paquetes MTS se hayan convertido realmente, pero que falten algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="91538-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="91538-108">En este caso, use la herramienta administrativa Servicios de componentes para comprobar todos los atributos.</span><span class="sxs-lookup"><span data-stu-id="91538-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="91538-109">Los atributos MTS seguirán presentes en el equipo (en el registro del sistema en HKEY \_ local \_ Machine \\ Microsoft \\ Transaction Server), pero solo serán accesibles a través de la utilidad regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="91538-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="91538-110">Después del último reinicio antes de que se muestre el cuadro de diálogo Inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="91538-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="91538-111">En el paso 2 se tratan las acciones de conversión que requieren acceso a la red (principalmente, creación de miembros de rol).</span><span class="sxs-lookup"><span data-stu-id="91538-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="91538-112">Si se produce un error en el paso 2 (debido a errores temporales de la red o del controlador de dominio), es posible volver a ejecutar la utilidad de conversión MTSTOCOM cualquier número de veces.</span><span class="sxs-lookup"><span data-stu-id="91538-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="91538-113">Para ello, en el símbolo del sistema o después de seleccionar **Ejecutar** en el menú **Inicio** , escriba lo siguiente: **% WINDIR \\ % system32 \\mtstocom.exe**.</span><span class="sxs-lookup"><span data-stu-id="91538-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="91538-114">Archivo de registro de MTSTOCOM</span><span class="sxs-lookup"><span data-stu-id="91538-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="91538-115">La utilidad MTSTOCOM genera un archivo de registro (mtstocom. log) en el directorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="91538-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="91538-116">Este archivo de registro mantiene un registro de la conversión de paquetes MTS a aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="91538-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="91538-117">Si se produjeron errores durante el proceso de conversión, siempre es una buena idea comprobar el archivo de registro para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="91538-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="91538-118">El archivo de registro detecta problemas comunes, como un usuario o una contraseña no válidos.</span><span class="sxs-lookup"><span data-stu-id="91538-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91538-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91538-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91538-120">Resultados y problemas de la conversión de COM+</span><span class="sxs-lookup"><span data-stu-id="91538-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="91538-121">Conversión manual desde MTS</span><span class="sxs-lookup"><span data-stu-id="91538-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="91538-122">Biblioteca de administración de MTS</span><span class="sxs-lookup"><span data-stu-id="91538-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



