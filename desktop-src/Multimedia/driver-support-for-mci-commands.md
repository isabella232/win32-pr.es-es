---
title: Compatibilidad del controlador con comandos MCI
description: Compatibilidad del controlador con comandos MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2aa2bb806e869adcf4355b8b43ac529240a5c35dfc8ce49d43672baf0bd976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526295"
---
# <a name="driver-support-for-mci-commands"></a>Compatibilidad del controlador con comandos MCI

Los controladores MCI proporcionan la funcionalidad para los comandos de MCI. El software del sistema realiza algunas tareas básicas de administración de datos, pero todos los controladores de MCI individuales controlan toda la reproducción, presentación y grabación multimedia.

Los controladores varían en cuanto a su compatibilidad con los comandos de MCI y las marcas de comandos. Dado que los dispositivos multimedia pueden tener funcionalidades muy diferentes, MCI está diseñado para permitir que los controladores individuales amplíen o reduzcan los conjuntos de comandos para que coincidan con las funcionalidades del dispositivo. Por ejemplo, el comando [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) forma parte del conjunto de comandos para secuenciadores DE MIDI, pero el controlador MCISEQ incluido con Windows no admite este comando. En el tema de referencia del comando record se explica que los dispositivos del tipo de dispositivo **sequencer** reconocen el comando; Esto no significa que todos los dispositivos de este tipo admitan el comando . Las aplicaciones deben usar [**el comando capability**](capability.md) [**(MCI \_ GETDEVCAPS)**](mci-getdevcaps.md)para determinar las funcionalidades de un dispositivo determinado.

 

 




