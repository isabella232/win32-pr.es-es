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
# <a name="driver-support-for-mci-commands"></a>Compatibilidad con controladores para comandos MCI

Los controladores MCI proporcionan la funcionalidad para los comandos MCI. El software del sistema realiza algunas tareas básicas de administración de datos, pero todos los controladores de MCI individuales controlan toda la reproducción, presentación y grabación multimedia.

Los controladores varían en su compatibilidad con los comandos MCI y las marcas de comandos. Dado que los dispositivos multimedia pueden tener funcionalidades muy diferentes, MCI está diseñado para permitir que los controladores individuales extiendan o reduzcan los conjuntos de comandos para que coincidan con las capacidades del dispositivo. Por ejemplo, el comando [**registro**](record.md) ([**\_ registro de MCI**](mci-record.md)) forma parte del conjunto de comandos para secuenciadores MIDI, pero el controlador MCISEQ incluido en Windows no admite este comando. El tema de referencia del comando registro explica que los dispositivos del tipo de dispositivo **Sequencer** reconocen el comando; Esto no significa que todos los dispositivos de este tipo admitan el comando. Las aplicaciones deben usar el comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar las capacidades de un dispositivo determinado.

 

 




