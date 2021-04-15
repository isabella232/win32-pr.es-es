---
title: Marcado automático de RAS
description: Una característica denominada \ 0034; conexión predeterminada \ 0034; se agregó al sistema en Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Marcado automático, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676247"
---
# <a name="ras-autodial"></a><span data-ttu-id="4c2e6-104">Marcado automático de RAS</span><span class="sxs-lookup"><span data-stu-id="4c2e6-104">RAS AutoDial</span></span>

<span data-ttu-id="4c2e6-105">Se ha agregado una característica denominada "conexión predeterminada" al sistema en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c2e6-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="4c2e6-106">Si se produce un error en el intento de conexión, el sistema comprueba si hay una coincidencia explícita (para nombre Winsock o nombre de recurso compartido) en la base de datos si no es así, marca la conexión predeterminada en caso de que haya alguna.</span><span class="sxs-lookup"><span data-stu-id="4c2e6-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="4c2e6-107">**Windows 2000:** Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede tener acceso al host, la característica de marcado automático puede iniciar automáticamente una operación de conexión de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="4c2e6-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="4c2e6-108">Para ello, el marcado automático busca en la base de datos de direcciones de red una entrada de libreta de teléfonos que pueda utilizar para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="4c2e6-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="4c2e6-109">**Windows NT 4,0:  ** RAS mantiene una base de datos con los nombres de Winsock y/o los nombres de recursos compartidos que se han alcanzado correctamente mientras una conexión RAS/VPN estaba activa.</span><span class="sxs-lookup"><span data-stu-id="4c2e6-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="4c2e6-110">Más adelante, cuando se produzca un error en un intento de conexión de Winsock o recurso compartido, el sistema comprobará esta base de datos y ofrecerá la marca de la conexión almacenada.</span><span class="sxs-lookup"><span data-stu-id="4c2e6-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




