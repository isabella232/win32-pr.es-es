---
title: Arquitectura de Administración remota de Windows
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
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793041"
---
# <a name="windows-remote-management-architecture"></a>Arquitectura de Administración remota de Windows

La arquitectura Administración remota de Windows consta de componentes en los equipos cliente y servidor. En la ilustración siguiente se muestran los componentes de ambos equipos, cómo interactúan los componentes con otros componentes y el protocolo que se usa para la comunicación entre los equipos.

![arquitectura de WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a>Cliente solicitante

Los siguientes componentes de WinRM residen en el equipo que ejecuta el script que solicita los datos.

-   Aplicación WinRM

    Esta es la herramienta de línea de comandos de **WinRM** o script que usa la API de scripting de WinRM para realizar llamadas para solicitar datos o para ejecutar métodos. Para obtener más información, consulte la [API de scripting de WinRM](winrm-scripting-api.md).

-   WSMAuto.dll

    Nivel de automatización que proporciona compatibilidad con scripting.

-   WsmCL.dll

    Nivel de la API de C dentro del sistema operativo.

-   API DE HTTP

    WinRM requiere compatibilidad con el transporte HTTP y HTTPS.

## <a name="responding-server"></a>Servidor que responde

Los siguientes componentes de WinRM residen en el equipo que responde.

-   API DE HTTP

    WinRM requiere compatibilidad con el transporte HTTP y HTTPS.

-   WSMAuto.dll

    Nivel de automatización que proporciona compatibilidad con scripting.

-   WsmCL.dll

    Nivel de la API de C dentro del sistema operativo.

-   WsmSvc.dll

    Servicio de [*escucha*](windows-remote-management-glossary.md) de WinRM.

-   WsmProv.dll

    Subsistema del proveedor.

-   WsmRes.dll

    Archivo de recursos.

-   WsmWmiPl.dll

    [*Complemento WMI*](windows-remote-management-glossary.md). Esto le permite obtener datos de WMI a través de WinRM.

-   Controlador de interfaz de administración de plataforma inteligente (IPMI) y proveedor IPMI de WMI

    Estos componentes proporcionan los datos de hardware solicitados mediante las clases de IPMI. Para obtener más información, consulte [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). El SMBIOS debe haber detectado hardware de BMC o el dispositivo creado manualmente cargando el controlador. Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> </dl>

 

 