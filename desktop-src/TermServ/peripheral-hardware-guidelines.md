---
title: Directrices de hardware de periféricos
description: Si su dispositivo de hardware no está diseñado para funcionar a través de una sesión remota, los proveedores deben asegurarse de que el software de controlador de dispositivo fuerce la deshabilitación de la redirección del dispositivo mediante una directiva del sistema o una directiva de grupo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418942"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="ea33a-103">Directrices de hardware de periféricos</span><span class="sxs-lookup"><span data-stu-id="ea33a-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="ea33a-104">En un cliente Conexión a Escritorio remoto (RDC), el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto) es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="ea33a-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="ea33a-105">Por lo tanto, los dispositivos como las unidades de disco y las impresoras conectadas al servidor aparecen como dispositivos locales para un cliente.</span><span class="sxs-lookup"><span data-stu-id="ea33a-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="ea33a-106">Por el contrario, las unidades e impresoras conectadas a un terminal cliente pueden parecer dispositivos remotos, dependiendo de las opciones seleccionadas para la conexión, el servidor utilizado y la versión del software cliente que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ea33a-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="ea33a-107">Aunque la versión inicial de Servicios de Escritorio remoto no admitía las aplicaciones que envían la salida directamente a los puertos serie, paralelos y de sonido conectados al terminal del cliente, las versiones actuales permiten que estos dispositivos aparezcan como dispositivos locales en las aplicaciones que se ejecutan en la sesión Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ea33a-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="ea33a-108">Si su dispositivo de hardware no está diseñado para funcionar a través de una sesión remota, los proveedores deben asegurarse de que el software de controlador de dispositivo fuerce la deshabilitación de la redirección del dispositivo mediante una directiva del sistema o una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ea33a-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




