---
title: Información del controlador de dispositivo
description: Los controladores de dispositivos y los módulos son similares, ya que ambos se basan en archivos PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075346"
---
# <a name="device-driver-information"></a>Información del controlador de dispositivo

Los controladores de dispositivos y los módulos son similares, ya que ambos se basan en archivos PE. Sin embargo, mientras que cada proceso tiene su propia lista privada de módulos cargados, los controladores de dispositivos tienen módulos que son globales para el sistema. Por lo tanto, PSAPI tiene funciones específicas para obtener la lista de controladores de dispositivos y sus nombres.

Puede recuperar la dirección de carga de cada controlador de dispositivo mediante una llamada a la función [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) . Esta función rellena una matriz de valores de **LPVOID** con las direcciones de carga de todos los controladores de dispositivos del sistema.

La función [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) toma una dirección de carga del controlador como entrada y rellena un búfer con el nombre base del controlador (por ejemplo, Win32k.sys). Una función relacionada, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), toma los mismos parámetros y devuelve la ruta de acceso al controlador de dispositivo (por ejemplo, C: \\ Windows \\ system32 \\Win32k.sys).

 

 




