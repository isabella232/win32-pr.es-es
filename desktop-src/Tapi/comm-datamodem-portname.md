---
description: La clase de dispositivo COMM/telemodem/portname se compone de los nombres de dispositivo a los que están conectados los módems.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: COMM/telemodem/portname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911538"
---
# <a name="commdatamodemportname"></a>COMM/telemodem/portname

La clase de dispositivo COMM/telemodem/portname se compone de los nombres de dispositivo a los que están conectados los módems. Cuando se especifica este nombre de dispositivo en una llamada a la función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) , la función rellena la estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) con una cadena ANSI (no Unicode) terminada en null que especifica el nombre del puerto al que está conectado el módem especificado, como "COM1 \\ 0". Esto está pensado principalmente para fines de identificación en la interfaz de usuario, pero se puede usar en algunas circunstancias para abrir el dispositivo directamente, omitiendo el proveedor de servicios (si el proveedor de servicios aún no tiene el dispositivo abierto). Si no hay ningún puerto asociado al dispositivo, se devuelve una cadena null (" \\ 0") en la estructura **VARSTRING** (con una longitud de cadena de 1).

 

 



