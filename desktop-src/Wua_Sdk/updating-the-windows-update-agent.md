---
description: Windows Update Agent (WUA) se actualiza automáticamente cuando se conecta a un servidor Windows Server Update Services (WSUS) o Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Actualizando Windows Update agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fe439b1bea377e2699f6fe5714b208ac5d951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715269"
---
# <a name="updating-windows-update-agent"></a>Actualizando Windows Update agente

Windows Update Agent (WUA) se actualiza a través de varios medios, en función de la versión de Windows que se ejecuta en el dispositivo. Es posible que las versiones anteriores de WUA no puedan conectarse a los servicios de actualización actuales, puede que no sean compatibles con todas las actualizaciones y puede que no sean compatibles con todas las API documentadas. Aquí se explica cómo asegurarse de que WUA está totalmente actualizado y es compatible.

**En las versiones de Windows a partir de Windows 7 y Windows Server 2008 R2**

Las actualizaciones periódicas del agente de Windows Update (WUA) se incluyen en las actualizaciones periódicas periódicas de Windows distribuidas a través de Windows Update o Windows Server Update Services (WSUS). No es necesario realizar ningún paso especial para actualizar WUA en estas versiones de Windows.

**En versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2**

WUA se actualiza automáticamente cuando Actualizaciones automáticas se conecta a Windows Update o a WSUS.

Si Actualizaciones automáticas aún no se ha ejecutado correctamente, es posible que un dispositivo que ejecute estas versiones de Windows Ejecute una versión anterior de WUA que no admita todas las API documentadas. Si recibe un WU_E_SELFUPDATE_REQUIRED resultado cuando usa la API de WUA para realizar un análisis, descarga o instalación, este error indica que la versión instalada de WUA es demasiado antigua para conectarse a los servicios de Windows Update actuales. No se pueden usar las API de WUA normales para actualizar WUA en estos sistemas operativos. 

Un usuario puede actualizar de forma manual el WUA a una versión actual; para ello, abra el panel de control de Windows Update, seleccione Buscar actualizaciones y acepte la actualización automática que aparece. Como alternativa, puede actualizar WUA mediante programación.

**Para actualizar el WUA mediante programación en versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2**

1.  Use las API de [WinHTTP](../winhttp/winhttp-start-page.md) para descargar [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
2.  Use las [funciones de criptografía](../seccrypto/cryptography-functions.md) para comprobar que la copia descargada de [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) tiene una firma digital de Microsoft. Si no puede comprobar la firma digital, detenga.
3.  Use las API de la [interfaz de descompresión de archivos](../devnotes/cabinet-api-functions.md) para extraer el archivo XML de [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Use las API de Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) para cargar el archivo XML y ubicar el nodo WURedist/StandaloneRedist/Architecture para la arquitectura del equipo. Por ejemplo, para x86, busque el nodo WURedist/StandaloneRedist/Architecture con el atributo **Name** de x86.
5.  Llame a [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para determinar la versión actual de WUA. Si **IWindowsUpdateAgentInfo:: GetInfo** devuelve un número de versión que es al menos tan alto como el atributo **clientVersion** en el nodo de arquitectura que encontró, detenga.
6.  Use las API de [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para leer el atributo **downloadUrl** del nodo de arquitectura que encontró. **downloadUrl** proporciona la dirección URL de descarga para el instalador de WUA adecuado para la arquitectura del equipo.
7.  Use las API de [WinHTTP](../winhttp/winhttp-start-page.md) para descargar el instalador adecuado.
8.  Use la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o una API similar para ejecutar el instalador descargado.

 

 
