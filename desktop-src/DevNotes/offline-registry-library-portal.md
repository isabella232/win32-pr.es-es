---
description: Biblioteca del Registro sin conexión
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Biblioteca del Registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed71e617c838d2f12196dd205a9a84dca9d0f9c8e6b27fcf5790bed65d19c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076109"
---
# <a name="offline-registry-library"></a>Biblioteca del Registro sin conexión

## <a name="purpose"></a>Propósito

La biblioteca del Registro sin conexión (Offreg.dll) se usa para modificar un subárbol del Registro fuera del registro del sistema activo. Esta biblioteca está pensada para escenarios de actualización del Registro, como el mantenimiento de una imagen de sistema operativo. La biblioteca admite formatos de Subárbol del Registro a partir Windows Vista.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta tecnología está disponible para fabricantes de equipos originales (OEM), proveedores de software antivirus y antimalware y otros desarrolladores de aplicaciones que deben poder analizar los archivos de Hive del Registro sin cargarlos en el registro activo.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La biblioteca del Registro sin conexión se proporciona como una biblioteca de vínculos dinámicos (DLL) redistribuible binaria. Esta biblioteca se ejecuta en las siguientes versiones de Windows:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

Las aplicaciones deben vincular a Offreg.dll mediante la vinculación dinámica.

Offreg.dll se proporciona en Windows Driver Kit (WDK) para Windows 10 versiones anteriores del Windows operativo.

Para obtener información sobre la obtención de WDK, vea [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) (Cómo obtener wdk y WLK) o visite el sitio web de suscripciones de [MSDN.](https://msdn.microsoft.com/subscriptions/default.aspx)

## <a name="in-this-section"></a>En esta sección

-   [**Acerca de la biblioteca del Registro sin conexión**](about-the-offline-registry-library.md)
-   [**Funciones de la biblioteca del Registro sin conexión**](offline-registry-library-functions.md)

 

 
