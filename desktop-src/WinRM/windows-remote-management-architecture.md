---
title: Administración remota de Windows arquitectura
description: La arquitectura Administración remota de Windows consta de componentes en los equipos cliente y servidor.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 889a823c4c67bed29f9ce695d84c893654b541aed76e0c79860e31f24c543662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121604"
---
# <a name="windows-remote-management-architecture"></a>Administración remota de Windows arquitectura

La arquitectura Administración remota de Windows consta de componentes en los equipos cliente y servidor. En la ilustración siguiente se muestran los componentes de ambos equipos, cómo interactúan los componentes con otros componentes y el protocolo que se usa para comunicarse entre los equipos.

![arquitectura winrm](images/winrm-architecture.png)

## <a name="requesting-client"></a>Solicitud de cliente

Los siguientes componentes de WinRM residen en el equipo que ejecuta el script que solicita datos.

-   Aplicación WinRM

    Se trata del script o la herramienta de línea de comandos **de Winrm** que usa la API de scripting de WinRM para realizar llamadas a para solicitar datos o ejecutar métodos. Para obtener más información, vea [WinRM Scripting API](winrm-scripting-api.md).

-   WSMAuto.dll

    La capa de Automation que proporciona compatibilidad con scripting.

-   WsmCL.dll

    Capa de API de C dentro del sistema operativo.

-   API DE HTTP

    WinRM requiere compatibilidad con el transporte HTTP y HTTPS.

## <a name="responding-server"></a>Servidor de respuesta

Los siguientes componentes de WinRM residen en el equipo que responde.

-   API DE HTTP

    WinRM requiere compatibilidad con el transporte HTTP y HTTPS.

-   WSMAuto.dll

    La capa de Automation que proporciona compatibilidad con scripting.

-   WsmCL.dll

    Capa de API de C dentro del sistema operativo.

-   WsmSvc.dll

    Servicio de escucha [*winRM.*](windows-remote-management-glossary.md)

-   WsmProv.dll

    Subsistema de proveedor.

-   WsmRes.dll

    Archivo de recursos.

-   WsmWmiPl.dll

    [*Complemento WMI*](windows-remote-management-glossary.md). Esto le permite obtener datos WMI a través de WinRM.

-   Controlador de interfaz de administración de plataforma inteligente (IPMI) y proveedor de IPMI WMI

    Estos componentes suministran los datos de hardware que se solicitan mediante las clases IPMI. Para obtener más información, vea [Proveedor DE IPMI.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) El hardware de BMC debe haber sido detectado por SMBIOS o el dispositivo creado manualmente mediante la carga del controlador. Para obtener más información, [vea Instalación y configuración de Administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> </dl>

 

 