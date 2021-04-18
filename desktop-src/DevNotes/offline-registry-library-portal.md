---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Biblioteca del registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666165"
---
# <a name="offline-registry-library"></a>Biblioteca del registro sin conexión

## <a name="purpose"></a>Propósito

La biblioteca del registro sin conexión (Offreg.dll) se utiliza para modificar un subárbol del registro fuera del registro del sistema activo. Esta biblioteca está pensada para escenarios de actualización del registro, como el mantenimiento de una imagen de sistema operativo. La biblioteca admite formatos de subárbol del registro a partir de Windows Vista.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta tecnología está diseñada para fabricantes de equipos originales (OEM), proveedores de software antivirus y antimalware, y otros desarrolladores de aplicaciones que deben poder analizar archivos de subárbol del registro sin cargarlos en el registro activo.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La biblioteca del registro sin conexión se proporciona como una biblioteca de vínculos dinámicos (DLL) redistribuible binaria. Esta biblioteca se ejecuta en las siguientes versiones de Windows:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

Las aplicaciones deben vincularse a Offreg.dll mediante la vinculación dinámica.

Offreg.dll se proporciona en Windows Driver Kit (WDK) para Windows 10 y versiones anteriores del sistema operativo Windows.

Para obtener información sobre cómo obtener el WDK, vea [Cómo obtener el WDK y WLK](/windows-hardware/drivers/download-the-wdk) o visite el sitio web de [suscripciones a MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .

## <a name="in-this-section"></a>En esta sección

-   [**Acerca de la biblioteca de registro sin conexión**](about-the-offline-registry-library.md)
-   [**Funciones de la biblioteca del registro sin conexión**](offline-registry-library-functions.md)

 

 
