---
description: Los proveedores de seguridad WMI se pueden usar para el scripting de WMI y para crear un proveedor de seguridad administrado.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Proveedores de seguridad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666383"
---
# <a name="security-wmi-providers"></a>Proveedores de seguridad WMI

## <a name="purpose"></a>Propósito

Los proveedores de seguridad de WMI permiten a los administradores y programadores configurar Cifrado de unidad BitLocker (BDE) y el Módulo de plataforma segura (TPM) mediante Instrumental de administración de Windows (WMI).

## <a name="developer-audience"></a>Audiencia de desarrolladores

Este documento especifica la interfaz del proveedor WMI para administrar y configurar Cifrado de unidad BitLocker (BDE) y Módulo de plataforma segura (TPM) en Windows Server 2008 R2 y Windows Server 2008 para servidores, y Windows 7 y Windows Vista para equipos cliente. Está diseñado para ser leído por los scripts de escritura, los elementos de la interfaz de usuario u otras herramientas administrativas para BDE o TPM.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Los proveedores de WMI de seguridad requieren el archivo. mof especificado con cada proveedor y un sistema operativo compatible. El sistema operativo mínimo es Windows Server 2008 o Windows Vista. Cifrado de unidad BitLocker solo está disponible para las versiones Windows Vista Enterprise y Windows Vista Ultimate de Windows Vista. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                               | Descripción                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Acerca de los proveedores de WMI de seguridad](about-security-wmi-providers.md)<br/>         | Breve introducción a los proveedores de WMI de seguridad.<br/>           |
| [Referencia de proveedores de WMI de seguridad](security-wmi-providers-reference.md)<br/> | Documentación de referencia de los proveedores de WMI de seguridad.<br/> |



 

## <a name="additional-resources"></a>Recursos adicionales

Los siguientes son recursos adicionales.



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clases<br/> | Para obtener más información acerca de los proveedores de WMI de seguridad, vea [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) y [**Win32 \_ TPM**](win32-tpm.md).<br/> |



 

 

 




