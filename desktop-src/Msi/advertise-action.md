---
description: La acción anunciar es una acción de nivel superior llamada para instalar o quitar componentes anunciados.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Acción de anuncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813350"
---
# <a name="advertise-action"></a><span data-ttu-id="f5590-103">Acción de anuncio</span><span class="sxs-lookup"><span data-stu-id="f5590-103">ADVERTISE Action</span></span>

<span data-ttu-id="f5590-104">La acción anunciar es una acción de nivel superior llamada para instalar o quitar componentes anunciados.</span><span class="sxs-lookup"><span data-stu-id="f5590-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f5590-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="f5590-105">Sequence Restrictions</span></span>

<span data-ttu-id="f5590-106">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f5590-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f5590-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="f5590-107">ActionData Messages</span></span>

<span data-ttu-id="f5590-108">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="f5590-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5590-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5590-109">Remarks</span></span>

<span data-ttu-id="f5590-110">La [*publicidad*](a-gly.md) se refiere a la capacidad del instalador de proporcionar las interfaces de carga e inicio de una aplicación sin necesidad de instalar físicamente la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5590-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="f5590-111">El instalador no instala los componentes necesarios hasta que un usuario o una aplicación Active una interfaz anunciada.</span><span class="sxs-lookup"><span data-stu-id="f5590-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="f5590-112">Este concepto se denomina [*instalación a petición*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f5590-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="f5590-113">No se llama a la acción de anuncio desde la secuencia de la tabla de acciones, la Windows Installer ejecuta esta acción cuando se llama al Msiexec.exe ejecutable de línea de comandos con el modificador de línea de comandos '/j ' o cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el parámetro *SZCOMMANDLINE* establecido en Action = resume.</span><span class="sxs-lookup"><span data-stu-id="f5590-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5590-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5590-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5590-115">Tabla AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f5590-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



