---
title: Compatibilidad con controladores para comandos MCI
description: Compatibilidad con controladores para comandos MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775121"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="a27be-103">Compatibilidad con controladores para comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a27be-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="a27be-104">Los controladores MCI proporcionan la funcionalidad para los comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="a27be-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="a27be-105">El software del sistema realiza algunas tareas básicas de administración de datos, pero todos los controladores de MCI individuales controlan toda la reproducción, presentación y grabación multimedia.</span><span class="sxs-lookup"><span data-stu-id="a27be-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="a27be-106">Los controladores varían en su compatibilidad con los comandos MCI y las marcas de comandos.</span><span class="sxs-lookup"><span data-stu-id="a27be-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="a27be-107">Dado que los dispositivos multimedia pueden tener funcionalidades muy diferentes, MCI está diseñado para permitir que los controladores individuales extiendan o reduzcan los conjuntos de comandos para que coincidan con las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a27be-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="a27be-108">Por ejemplo, el comando [**registro**](record.md) ([**\_ registro de MCI**](mci-record.md)) forma parte del conjunto de comandos para secuenciadores MIDI, pero el controlador MCISEQ incluido en Windows no admite este comando.</span><span class="sxs-lookup"><span data-stu-id="a27be-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="a27be-109">El tema de referencia del comando registro explica que los dispositivos del tipo de dispositivo **Sequencer** reconocen el comando; Esto no significa que todos los dispositivos de este tipo admitan el comando.</span><span class="sxs-lookup"><span data-stu-id="a27be-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="a27be-110">Las aplicaciones deben usar el comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar las capacidades de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="a27be-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




