---
description: Windows El Agente de actualización (WUA) se actualiza automáticamente cuando está conectado a un servidor Windows Server Update Services (WSUS) o a Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Actualizar Windows Update Agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388475aaf9fa83413a916520035eb9539187390bf5a3bd8f5c836cb1b176357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814656"
---
# <a name="updating-windows-update-agent"></a>Actualizar Windows Update Agent

Windows El Agente de actualización (WUA) se actualiza a sí mismo a través de varios medios, en función de la versión de Windows que se ejecuta en el dispositivo. Es posible que las versiones anteriores de WUA no puedan conectarse a los servicios de actualización actuales, que no sean compatibles con todas las actualizaciones y que no admitan todas las API documentadas. Aquí se muestra cómo garantizar que WUA está totalmente actualizado y es compatible.

**En versiones de Windows a partir de Windows 7 y Windows Server 2008 R2**

Windows Las actualizaciones del Agente de actualización (WUA) se incluyen en las actualizaciones periódicas periódicas de Windows se distribuyen a través de Windows Update o Windows Server Update Services (WSUS). No es necesario realizar ningún paso especial para actualizar WUA en estas Windows versiones.

**En versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2**

WUA se actualiza automáticamente cuando Actualizaciones automáticas se conecta a Windows Update o a WSUS.

Si Actualizaciones automáticas se ha ejecutado correctamente, es posible que un dispositivo que ejecute estas versiones de Windows ejecute una versión anterior de WUA que no admita todas las API documentadas. Si recibe un resultado WU_E_SELFUPDATE_REQUIRED cuando usa la API de WUA para realizar un examen, descargar o instalar, este error le indica que la versión instalada de WUA es demasiado antigua para conectarse a los servicios de actualización de Windows actuales. No puede usar las API de WUA normales para actualizar WUA en estos sistemas operativos. 

Un usuario puede actualizar manualmente WUA a una versión actual; para ello, abra el panel de control de actualización de Windows, seleccione Buscar actualizaciones y, a continuación, acepte la actualización automática que aparece. Como alternativa, puede actualizar WUA mediante programación.

**Para actualizar WUA mediante programación en versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2**

1.  Use las [API WinHTTP](../winhttp/winhttp-start-page.md) para descargar [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
2.  Use las [funciones de criptografía](../seccrypto/cryptography-functions.md) para comprobar que la copia descargada de [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) tiene una firma digital de Microsoft. Si no puede comprobar la firma digital, detenga.
3.  Use las [API de la interfaz de descompresión](../devnotes/cabinet-api-functions.md) de archivos para extraer el archivo XML de [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Use las API Microsoft XML Core Services[(MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) para cargar el archivo XML y buscar el nodo WURedist/StandaloneRedist/architecture para la arquitectura del equipo. Por ejemplo, para x86, busque el nodo WURedist/StandaloneRedist/architecture con el atributo **name** de x86.
5.  Llame [**a IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para determinar la versión actual de WUA. Si **IWindowsUpdateAgentInfo::GetInfo** devuelve un número de versión que es al menos tan alto como el atributo **clientVersion** en el nodo de arquitectura que ha ubicado, detenga.
6.  Use el [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API para leer el atributo **downloadUrl** del nodo de arquitectura que ha ubicado. **downloadUrl** proporciona la dirección URL de descarga del instalador de WUA adecuado para la arquitectura del equipo.
7.  Use las [API winHTTP](../winhttp/winhttp-start-page.md) para descargar el instalador adecuado.
8.  Use la [**función CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o una API similar para ejecutar el instalador descargado.

 

 
