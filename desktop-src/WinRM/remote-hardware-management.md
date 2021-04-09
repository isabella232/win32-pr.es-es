---
title: Administración remota de hardware
description: Administración remota de hardware
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Administración remota de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bbb470d513b49d2158865c4c42051cc16856ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791697"
---
# <a name="remote-hardware-management"></a>Administración remota de hardware

Administración remota de Windows la administración de hardware está diseñada para reducir los costos generales de administración de TI mediante la supervisión y el control de los componentes de hardware remotos, especialmente antes de que se inicie el sistema y después de un error del sistema operativo.

Los fabricantes de equipos originales (OEM) han desarrollado una arquitectura común para satisfacer la necesidad de administración de hardware. Una parte importante de esta arquitectura es el [*controlador de administración de placa base*](windows-remote-management-glossary.md) (BMC). Un BMC es un dispositivo especializado que supervisa el estado del equipo servidor. El BMC proporciona control remoto del hardware del servidor, recupera datos de estado y recibe notificaciones sobre los errores críticos y otros cambios de estado de hardware. Un script o una aplicación que está supervisando un servidor remoto puede obtener datos del servidor, ya sea [*en banda*](windows-remote-management-glossary.md), a través del sistema operativo remoto o [*fuera de banda*](windows-remote-management-glossary.md), directamente desde el BMC.

Un BMC tiene sensores que pueden detectar, por ejemplo, cuando el equipo servidor se está sobrecalentaendo o cuando el voltaje está fuera del intervalo aceptable. Existen varios estándares para definir la arquitectura de BMC. La [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md) es un estándar de este tipo que se usa con frecuencia. Sin embargo, a pesar del estándar IPMI, el acceso de administración al hardware del servidor es propietario y requiere el uso de las herramientas de administración proporcionadas por los OEM. Además, el acceso remoto a un BMC se proporciona mediante un protocolo de conexión especializada, el protocolo de control de administración remota (RMCP), que tiene mecanismos de seguridad no estándar para la autenticación de acceso.

El [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) de Microsoft y el controlador IPMI permiten obtener datos de BMC de equipos de servidores remotos a través de un proveedor WMI estándar con [clases](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI. Aunque puede escribir un script de WMI normal que obtenga datos remotos a través de DCOM, en muchos casos el método preferido para obtener datos de IPMI es mediante la utilidad de línea de comandos de **WinRM** o la API de [scripting](winrm-scripting-api.md) de WinRM o la [API de C++ de WinRM](winrm-c---api.md). La utilidad WinRM y las API del servicio WinRM se basan en el protocolo WS-Management y pueden obtener datos IPMI desde un equipo local o remoto sin usar DCOM.

El BMC también tiene una base de datos de eventos denominada registro de eventos del sistema (SEL) que registra los eventos en el equipo supervisado. No se puede suscribir para que estos eventos se entreguen a un script como se puede hacer con las clases de eventos de WMI. Sin embargo, puede usar la herramienta de línea de comandos Wecutil.exe para suscribirse a ellas. Para obtener más información sobre cómo usar esta herramienta, escriba **wecutil/?** en el símbolo del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> </dl>

 

 