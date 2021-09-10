---
title: Compatibilidad del controlador con comandos MCI
description: Compatibilidad del controlador con comandos MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371618"
---
# <a name="driver-support-for-mci-commands"></a>Compatibilidad del controlador con comandos MCI

Los controladores de MCI proporcionan la funcionalidad para los comandos de MCI. El software del sistema realiza algunas tareas básicas de administración de datos, pero todos los controladores de MCI individuales controlan toda la reproducción, presentación y grabación multimedia.

Los controladores varían en su compatibilidad con los comandos de MCI y las marcas de comandos. Dado que los dispositivos multimedia pueden tener funcionalidades muy diferentes, MCI está diseñado para permitir que los controladores individuales amplíen o reduzcan los conjuntos de comandos para que coincidan con las funcionalidades del dispositivo. Por ejemplo, el comando [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) forma parte del conjunto de comandos para secuenciadores DE LÍNEA, pero el controlador MCISEQ incluido con Windows no admite este comando. En el tema de referencia del comando record se explica que los dispositivos del tipo de dispositivo **sequencer** reconocen el comando; Esto no significa que todos los dispositivos de este tipo admitan el comando . Las aplicaciones deben usar [**el comando capability**](capability.md) [**(MCI \_ GETDEVCAPS)**](mci-getdevcaps.md)para determinar las funcionalidades de un dispositivo determinado.

 

 




