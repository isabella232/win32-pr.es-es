---
title: Información del controlador de dispositivo
description: Los controladores de dispositivos y los módulos son similares en que ambos se basan en archivos PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf8539a676f178736170afd04d9069275b6a3b56c9c80ef169d9e33d7d38f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944445"
---
# <a name="device-driver-information"></a>Información del controlador de dispositivo

Los controladores de dispositivos y los módulos son similares en que ambos se basan en archivos PE. Sin embargo, aunque cada proceso tiene su propia lista privada de módulos cargados, los controladores de dispositivos tienen módulos que son globales para el sistema. Por lo tanto, PSAPI tiene funciones específicas para obtener la lista de controladores de dispositivos y sus nombres.

Puede recuperar la dirección de carga de cada controlador de dispositivo llamando a la [**función EnumDeviceDrivers.**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) Esta función rellena una matriz de valores **LPVOID** con las direcciones de carga de todos los controladores de dispositivo del sistema.

La [**función GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) toma una dirección de carga del controlador como entrada y rellena un búfer con el nombre base del controlador (por ejemplo, Win32k.sys). Una función relacionada, [**GetDeviceDriverFileName,**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea)toma los mismos parámetros y devuelve la ruta de acceso al controlador de dispositivo (por ejemplo, C: \\ Windows \\ System32 \\Win32k.sys).

 

 




