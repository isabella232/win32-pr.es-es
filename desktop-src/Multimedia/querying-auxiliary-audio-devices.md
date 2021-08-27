---
title: Consulta de dispositivos de audio auxiliares
description: Consulta de dispositivos de audio auxiliares
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- audio de onda, consulta de dispositivos de audio auxiliares
- audio auxiliar, consultar dispositivos
- interfaz de audio auxiliar
- dispositivos de audio auxiliares, consulta
- consultar dispositivos de audio auxiliares
- audio auxiliar, interfaz
- audio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a6d61634475c3b921428529df69113c921b8c5bff8d1a65d5b08931a670fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037575"
---
# <a name="querying-auxiliary-audio-devices"></a>Consulta de dispositivos de audio auxiliares

No todos los sistemas multimedia tienen compatibilidad de audio auxiliar. Puede usar la [**función auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) para determinar el número de dispositivos auxiliares controlables presentes en un sistema.

Para obtener información sobre un dispositivo de audio auxiliar determinado, use la [**función auxGetDevCaps.**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) Esta función rellena una estructura [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) con información sobre las funcionalidades de un dispositivo especificado. Esta información incluye los identificadores de fabricante y producto, un nombre de producto para el dispositivo y el número de versión del controlador de dispositivo.

 

 