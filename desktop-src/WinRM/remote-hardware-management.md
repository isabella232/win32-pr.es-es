---
title: Administración remota de hardware
description: Administración remota de hardware
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Administración remota de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db94c1f50b05f5180504ecef68bf10b1a5a596c9a9f88b96e7c5efb9faaa89bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858735"
---
# <a name="remote-hardware-management"></a>Administración remota de hardware

Windows La administración remota de hardware está pensada para reducir los costos generales de administración de IT al proporcionar supervisión y control de los componentes de hardware remoto, especialmente antes de que se inicia el sistema y después de un error del sistema operativo.

Los fabricantes de equipos originales (OEM) han desarrollado una arquitectura común para abordar la necesidad de administración de hardware. Una parte importante de esta arquitectura es el [*controlador de administración de placa base*](windows-remote-management-glossary.md) (BMC). Un BMC es un dispositivo especializado que supervisa el estado del equipo servidor. El BMC proporciona control remoto del hardware del servidor, recupera datos de estado y recibe notificaciones sobre errores críticos y otros cambios de estado de hardware. Un script o aplicación que supervisa un servidor remoto puede obtener datos del servidor en [*banda,*](windows-remote-management-glossary.md)a través del sistema operativo remoto o fuera de [*banda,*](windows-remote-management-glossary.md)directamente desde el BMC.

Un BMC tiene sensores que pueden detectar, por ejemplo, cuándo se está sobresaliendo el equipo servidor o cuando el voltaje está fuera del intervalo aceptable. Existen varios estándares para definir la arquitectura de BMC. La [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md) es uno de estos estándares que se usa con frecuencia. Sin embargo, a pesar del estándar IPMI, el acceso de administración al hardware del servidor es propietario y requiere el uso de las herramientas de administración proporcionadas por los OEM. Además, el acceso remoto a un BMC se proporciona mediante un protocolo de conexión especializado, Protocolo de control de administración remota (RMCP), que tiene mecanismos de seguridad no estándar para la autenticación de acceso.

El proveedor [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) de Microsoft y el controlador IPMI permiten obtener datos de BMC de equipos de servidor remotos a través de un proveedor WMI estándar con [clases](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI . Aunque puede escribir un script WMI normal que obtenga datos remotos a través de DCOM, en muchos casos el método preferido para obtener datos IPMI es a través de la utilidad de línea de comandos **Winrm,** la API de scripting de [WinRM](winrm-scripting-api.md) o la API de C++ de [WinRM.](winrm-c---api.md) La utilidad Winrm y las API del servicio WinRM se basan en el protocolo WS-Management y pueden obtener datos IPMI desde un equipo local o remoto sin usar DCOM.

El BMC también tiene una base de datos de eventos denominada Registro de eventos del sistema (SEL) que registra eventos en el equipo supervisado. No puede suscribirse para que estos eventos se entreguen a un script como se puede hacer con las clases de eventos WMI. Sin embargo, puede usar la herramienta Wecutil.exe línea de comandos para suscribirse a ellos. Para obtener más información sobre cómo usar esta herramienta, en un símbolo del sistema, escriba **wecutil /?**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> </dl>

 

 