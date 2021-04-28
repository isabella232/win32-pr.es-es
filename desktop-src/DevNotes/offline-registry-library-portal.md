---
description: Biblioteca del Registro sin conexión
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Biblioteca del Registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089253"
---
# <a name="offline-registry-library"></a>Biblioteca del Registro sin conexión

## <a name="purpose"></a>Propósito

La biblioteca del Registro sin conexión (Offreg.dll) se usa para modificar un subárbol del Registro fuera del registro del sistema activo. Esta biblioteca está pensada para escenarios de actualización del Registro, como el mantenimiento de una imagen de sistema operativo. La biblioteca admite formatos de Subárbol del Registro a partir de Windows Vista.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta tecnología es para fabricantes de equipos originales (OEM), proveedores de software antivirus y antimalware y otros desarrolladores de aplicaciones que deben poder analizar los archivos de Hive del registro sin cargarlos en el registro activo.

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

Offreg.dll se proporciona en el Kit para controladores de Windows (WDK) para Windows 10 versiones anteriores del sistema operativo Windows.

Para obtener información sobre cómo obtener wdk, vea Cómo obtener [wdk](/windows-hardware/drivers/download-the-wdk) y WLK o visite el sitio web [de suscripciones de MSDN.](https://msdn.microsoft.com/subscriptions/default.aspx)

## <a name="in-this-section"></a>En esta sección

-   [**Acerca de la biblioteca del Registro sin conexión**](about-the-offline-registry-library.md)
-   [**Funciones de la biblioteca del Registro sin conexión**](offline-registry-library-functions.md)

 

 
